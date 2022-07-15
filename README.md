# JSON Lab

## Learning Goals

- Work with JSON files in Java

## Instructions

Modify your previous lab (CSV Lab) by adding the ability to save the list of
persons as JSON in addition to saving it as CSV.

Hints:

- To save as JSON, use the output from the `printPersonListAsJSON()` method and
  save it to file using the `writeToFile()` method.
- In order for the Jackson library to be able to create an instance of your
  `PersonServices.Person` class from its JSON representation, it needs to have a default
  constructor in the `PersonServices.Person` class, so simply add the following to your class:
  `public PersonServices.Person() {}`.
- To read from JSON, use the following method from the Jackson library:

```java
  List<PersonServices.Person> restoredPersons = Arrays.asList(new ObjectMapper().readValue(new File(PERSON_LIST_JSON_FILENAME), PersonServices.Person[].class));
```
