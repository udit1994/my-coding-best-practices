# Coding practices for writing Javascript/react application

_Disclaimer: I prefer to write this my code following these guideline. Feel free to adopt or ignore._

## Imports

- Segregate the imports to 2 groups, one consisting imports from node-modules and other from project source folder.
- Sort the individual group alphabetically.

## Objects

- Sort the object keys alphabetically.

## Types

- Define the types after the imports or is a separate folder for reusability.
- Avoid exporting types from files containing react component.

## Props

- In case of functional component, expoand the props within the function brackets `()`
- In case of class component, expand the component as the first thing or after the return null statement inside the member functions.
- Sort the props while calling the component.

## Exports

- Export ONE thing from a file, _Separation of concerns_
