#  React Important Questions

## 1. What is React?
- React is a front-end and open-source JavaScript library which is useful in developing user interfaces specifically for applications with a single page. It is helpful in building complex and reusable user interface(UI) components of mobile and web applications as it follows the component-based approach.

  **The important features of React are:**
  - It supports server-side rendering.
  - It will make use of the virtual DOM rather than real DOM (Data Object Model) as RealDOM manipulations are expensive.
  - It follows unidirectional data binding or data flow.
  - It uses reusable or composable UI components for developing the view.
 
## 2. What are the advantages of using React?
**MVC is generally abbreviated as Model View Controller**
- **Use of Virtual DOM to improve efficiency:** React uses virtual DOM to render the view. As the name suggests, virtual DOM is a virtual representation of the real DOM. Each time the data changes in a react app, a new virtual DOM gets created. Creating a virtual DOM is much faster than rendering the UI inside the browser. Therefore, with the use of virtual DOM, the efficiency of the app improves.
- **Gentle learning curve:** React has a gentle learning curve when compared to frameworks like Angular. Anyone with little knowledge of javascript can start building web applications using React.
- **SEO friendly:** React allows developers to develop engaging user interfaces that can be easily navigated in various search engines. It also allows server-side rendering, which boosts the SEO of an app.
- **Reusable components:** React uses component-based architecture for developing applications. Components are independent and reusable bits of code. These components can be shared across various applications having similar functionality. The re-use of components increases the pace of development.
- **Huge ecosystem of libraries to choose from:** React provides you with the freedom to choose the tools, libraries, and architecture for developing an application based on your requirement.

## 3. What are the limitations of React?
  **Here are some of the limitations of React:**
  - **It is a library, not a framework.** React is a library, which means that it provides a set of building blocks that you can use to create your own user interfaces. However, it does not provide everything you need to build a complete application. For example, React does not have built-in routing or state management. You will need to use third-party libraries for these features.
  - **Performance.** React applications can be slow if they are not properly optimized. This is because React re-renders the entire component tree whenever the state changes.
  - **VirtualDom** Virtual Dom is Fast but what it come to Dom Manupulation it is Quiet hard to Manupulate Real Dom (For ex - Animations etc).

## 4. What are React elements?
  **A React element is an object that represents a piece of UI. It is the smallest building block of a React application. React elements are created using React Apis but it is hard for Novice Developer and when the App become Large it is hard to handle so JSX come in rescue us, which is a syntax extension to JavaScript.**
  ### **For example, the following JSX code creates a React element that represents a button:**
  ```
//This is Button made using JSX
<button>Click me</button>
  ```
## 5. Benefit of using JSX?
**Here are some of the benefits of using JSX:**
- They are easy to create and understand.
- It makes your code more maintainable.
- It makes your code more performant.

## 6. Benefit of using React elements?
**Here are some of the benefits of using React elements:**
  - They are easy to create and understand.
  - They are immutable, which makes React applications more efficient.
  - They are virtual, which allows React to perform optimizations.
  - They are the foundation of React applications.

## 7. what are keys in React?
- **In React, a key is a special string attribute that you need to include when creating lists of elements. Keys are used to identify which items in the list have changed, updated, or deleted. This is important for React to be able to efficiently update the DOM when the state of your application changes.**
- **Keys must be unique within their parent component. This means that you cannot use the same key for two different elements in the same parent component. You can, however, use the same key for elements in different parent components.**
- 
  ```const numbers = [1, 2, 3, 4, 5];
 const listItems = numbers.map((number) => (
  <li key={number}>
    {number}
  </li>
));```
