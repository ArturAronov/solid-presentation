## Objectives when learning SolidJS

1. Learn new FE library/framework
2. Learn something new without Youtube. Only official documentation and SO allowed.

## About SolidJS

1. Built on Vite package bundler
   - Vite created by Evan You (who also created Vue)
   - Solid created by Ryan Carniato in 2018
   - Doesn't generate JS bundle unless the application is built
   - No virtual DOM, only uses just-in-time compiler
   - Very lightweight - 6.5kb
   - Component only renders once, signals can be updated multiple times without component re-render
2. Uses Signals as state handlers
3. Easier global states
   - https://github.com/ArturAronov/flashcards/blob/main/src/states/useCollection.tsx
4. Highly opinionated
5. No dependencies required in createEffect, managing side effects and dependencies can be quite difficult
   - https://github.com/ArturAronov/flashcards/blob/main/src/components/modals/ModalEditQuestionAnswer.tsx
6. Signals consist of Getter and Setter. Getter is a function
7. Has onMount and onCleanup functions available
8. `<Show when={} fallback={}></Show>` for conditional logic
   - https://github.com/ArturAronov/soldjs/blob/main/src/AddBook.tsx
9. `<For each={}>{(item) => <div>{item}</div>}</For>` for looping
   - https://github.com/ArturAronov/soldjs/blob/main/src/BookList.tsx
10. `createResource` for fetching data when Signal gets updated. `createResource` has access to `data.loading` and `data.error`
    - https://github.com/ArturAronov/soldjs/blob/main/src/AddBook.tsx
