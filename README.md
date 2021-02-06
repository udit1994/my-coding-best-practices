# Coding practices for writing Javascript/react application

_Disclaimer: I prefer to write this my code following these guideline. Feel free to adopt or ignore._

1. ### Imports

Imports can be a lot and messy, especially if you have named exports. Developer should not be spending a lot of time handling them. For example, grouping them based on their functionality like hooks, utils, etc.

I generally,

- Segregate the imports to 2 groups, one consisting imports from node-modules and other from project source folder.
- Sort the individual group alphabetically.

2. ### Objects

Javscript is all about objects. As our application grow we need to add/remove certain properties, it can be a headache for future developers to find the fields to add/remove. Do them a favour and always

- Sort the object keys alphabetically.

3. ### Exports

- Export ONE thing from a file, _Separation of concerns_.
- Always use default export.

4. ### Test cases

_WHERE TO KEEP TEST CASES?_

This is debatable, go around in the team, take a vote and decide. I prefer a folder replicating the exact src folder. And all the test cases within it. I then open two instances of VS code and work.

5. ### Typescript

Typescript is awesome but it comes at a cost of lot extra symbols, try keep your files as light as possible.

- Define the types in a separate folder.
- Avoid exporting types from files containing react component. It's just messy.

6. ### Code flow

- Write code that flows naturally. Use your judgement. Read before commiting.
- Don't force atomicity. Use _Separation of concerns_ and your judgement to disntegerate the code.

7. ### Performace

- Follow tree shaking best practices, like

```
  className.do(methodName)
```

This allows you to write functions outside of your class and when bundling only the methods used will go in the bundle.

Test performance using dev tools or

```
console.time("...")

performance.now("...")
```

## React

_React Docs already mentions lot of best practises, do follow them. Read famous github repos for best practice, and tricks. Render props is very powerful, when it comes to code reusability._

8. ### Props

- In case of functional component, expand the props within the function brackets `({...})`
- In case of class component, expand the component as the first thing or after the return null statement inside the member functions.
- Sort the props while calling the component.

9. ### Render functions

- In case of `return null` or similar stmt, put it as early as possible and put all the unnecessary login after that.

10. ### Hooks

- Use useMemo() and useCallback() wisely.

_\*WILL KEEP UPDATING\*_
