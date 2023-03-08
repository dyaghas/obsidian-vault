#sql 

An **entity-relationship model** illustrates how `entities` such as objects, people or concepts relate to each other within a system. They are often used to design or debug relational databases, mirroring grammatical structure, with entities as nouns and relationships as verbs.

The entity-relationship model has three main components; entity, attribute and relationship.

## Entity

a definable thing such as a concept, person or object. An entity can have a `type`, `set` and `category`.

![[erm-entity-image.png]]

- `Type`: student, teacher, driver... anything that can group entities together;
- `Set`:  same as an entity type, but defined at a particular point in time, such as students enrolled in a class on the first day;
- `Category`: entities are categorized as strong, weak or associative. A strong entity can be defined solely by its own attributes, while a weak entity cannot. An associative entity associates entities (or elements) within an entity set.
- `Entity key`: refers to an attribute that uniquely defines an entity in an entity set.

## Relationship

A relationship is how entities act upon each other or are associated with each other. Think of it as verbs. For example, the named student might register for a course.

![[erm-relationship.png]]

## Attribute

The attribute is used to describe the property of an entity. It is represented by a circle

![[erm-attribute.png]]

- `Primary key`: a special attribute with a unique value that identifies an instance of an entity. Every entity must have a primary key, which is represented by a black circle.

![[erm-primary-key.png]]