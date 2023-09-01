#mainframe

[[Mainframe]]
[[USS]]
## Job

JCL is used to describe to the system exactly what you want it to do. The task which we hand over to the system is known as a `Job`, and the component of z/OS that accepts, processes, and manages the output of these jobs is known as the Job Entry Subsystem (JES).

-----------------------------
## Symbolic

a variable prefixed with a `&`. Its value is replaced with a usable one when the code is run. For example:

```JCL
//JCLSETUP JOB ,MSGLEVEL=(0,0)
//     EXEC PGM=IEFBR14
//LOAD   DD DSN=&SYSUID..LOAD,DISP=(,CATLG),DATACLAS=SLOAD,
//       SPACE=(TRK,(1,1,2))
//JCL    DD DSN=&SYSUID..JCL,DISP=(,CATLG),DATACLAS=SPDS,
//       SPACE=(TRK,(1,1,2))
//SOURCE DD DSN=&SYSUID..SOURCE,DISP=(,CATLG),DATACLAS=SPDS,
//       SPACE=(TRK,(1,1,2))
//OUTPUT DD DSN=&SYSUID..OUTPUT,DISP=(,CATLG),DATACLAS=SPDS,
//       SPACE=(TRK,(1,1,2))
```

There is a symbolic `&SYSUID` in line 3 that is replaced with the current user id so it does not have to be inserted manually.

--------------------
# Learning the basics with examples

```JCL
//JCL2    JOB ,MSGLEVEL=(2,0)
//EXP EXPORT SYMLIST=*
//BEFORE   EXEC PGM=IKJEFT01,PARM='%PREJCL2'
//SYSPROC  DD DSN=ZXP.PUBLIC.EXEC,DISP=SHR
//SYSTSPRT DD SYSOUT=*
//SYSTSIN  DD DUMMY
//COBRUN  EXEC IGYWCL
//COBOL.SYSIN  DD DSN=ZXP.PUBLIC.SOURCE(CBL0001),DISP=SHR
//LKED.SYSLMOD DD DSN=&SYSUID..LOAD(CBL0001),DISP=SHR
//***************************************************/
// IF RC = 0 THEN
//***************************************************/
//RUN     EXEC PGM=CBL0001
//STEPLIB   DD DSN=&SYSUID..LOAD,DISP=SHR
//FNAMES    DD DSN=ZXP.PUBLIC.INPUT(FNAMES),DISP=SHR
//LNAMES    DD DSN=ZXP.PUBLIC.INPUT(LNAMES),DISP=SHR
//COMBINED   DD DSN=&SYSUID..OUTPUT(NAMES),DISP=SHR
//SYSOUT    DD SYSOUT=*,OUTLIM=15000
//CEEDUMP   DD DUMMY
//SYSUDUMP  DD DUMMY
//***************************************************/
// ELSE
// ENDIF
//AFTER    EXEC PGM=IKJEFT1A
//SYSTSPRT DD SYSOUT=*
//SYSTSIN  DD *,SYMBOLS=EXECSYS
LISTDS '&SYSUID..OUTPUT(NAMES)'
```

--------------------------------
## DD Statement

A Data Definition statement also called DD Statement defines where data is going from or going to.

--------------

## Step

in `JCL`, every new `step` begins with an line that contains the `EXEC` keyword

---------------------------

## RUN

The lines following the start of the //RUN step have the same format: 

```JCL
//"ddname" DD DSN="dataset",DISP="access"
```

- “ddname” is also known as the file name - the name used by programs to access data in datasets
- “dataset” is the actual location of the data - this can change, but the program doesn’t need to be aware
- `DISP` (disposition) parameters are used to describe how JCL should use or create a data set, and what to do with it after the job, or job step, completes.

	A standard DISP parameter has three parts. The first parameter is the status, which can be any of the following:
	
	![[Pasted image 20230830143525.png]]
	
	Field 2 of the DISP parameter describes what should happen to the dataset in the case of a normal completion, and the third field is what should happen to it in the case of a failure.
	
	There are a number of values we can use here, but for this challenge, here are some examples:
	
	![[Pasted image 20230830143842.png]]