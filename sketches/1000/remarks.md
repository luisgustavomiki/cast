## Scenario
Acme is a global corporation that, for some reason, much of its inputs to the business outputs can be expressed as tasks.
`acme-global-tasks` was then built as the bare minimum for a relevant understanding of those tasks.
Because Acme is such a big company, some of its critical operations reside within a software development context.
After a lot of misunderstandings and discomfort, developers and their peers and leaders felt like it was time for a casting of that framework for their reality.
`acme-software-tasks` was then built as a very specific outline of the development process they have created from scrum.

`acme-global-tasks` is led by the `task` symbol, which outlines a record type for a given task with the following fields:
 - `index` as a natural number, specified from an implicit standard symbol
 - `type` as an enum item, specified from an explicit symbol with the same name
 - `status` as the same as type
 - `summary` as a paragraph of text, specified from an implicit standard symbol
 - `person` as a composite record item, specified from an explicit symbol with the same name

`acme-software-tasks` is led by the `story` symbol, which outlines a record type for a given development user story task with the following fields:
 - `index`
 - `status`
 - `user-story`
 - `acceptance-criteria`

## Structure
A symbol has three parts:
 - `about` gives it a name and sets a note
 - `frame` outlines its contents
 - `specs` details the frame

## Enum/struct duality
A symbol might outline and specify a composite data type (struct) or a disjoint union (enum). This sketch does not discriminate between them within their definition. Instead, a dependant symbol will be responsible for interpreting it.
 - `is-enumerator-of` tells the system that a valid value to this field is an enumerator member of the referenced symbol
 - `is-value-of` tells the system that a valid value to this field is a subtype of the referenced symbol
 