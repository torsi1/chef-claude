# Chef Claude - AI-Powered Recipe Generator

Chef Claude is a modern React application built as part of the **Scrimba React Course**. The app allows users to create a dynamic list of ingredients and uses an AI model to suggest a recipe based on the items provided.



## Features

- **Dynamic Ingredient List:** Add ingredients seamlessly using the `FormData` API.
- **Conditional UI:** The "Get a Recipe" section only appears once you have at least 3 ingredients.
- **AI Integration:** Leverages an AI model (via Hugging Face) to generate creative recipes from your list.
- **Responsive Layout:** A clean, chef-themed interface that works on all screen sizes.
- **Modern React:** Built using functional components and the latest Hooks.

## Technologies Used

- **React 18** (Functional Components, Hooks)
- **CSS3** (Flexbox and modern styling)
- **Vite** (Fast build tool and dev server)
- **Hugging Face Inference API** (For recipe generation)

## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/torsi1/chef-claude.git](https://github.com/torsi1/chef-claude.git)

2. **Navigate to the directory:**
   ```bash
   cd chef-claude
   
3. **Install dependencies:**
   ```bash
   npm install

4. **Run the app:**
   ```bash
   npm run dev

## Key Learnings & Technical Focus

This project was a deep dive into several core React concepts:

* **State Management:** I used the `useState` hook to manage the array of ingredients. I learned how to update state immutably using the spread operator (`[...prevIngredients, newIngredient]`) to ensure React correctly tracks changes.
* **Form Handling:** Instead of syncing every keystroke to state (controlled components), I implemented the **uncontrolled components** pattern using the native `FormData` API. This approach leads to cleaner code and better performance by reducing unnecessary re-renders.
* **Conditional Rendering:** I developed logic to dynamically show or hide the recipe section and the "Get a Recipe" button based on the number of ingredients added to the list (minimum 3 required).
* **Side Effects:** Practiced using the `useEffect` hook to handle synchronization, such as scrolling the recipe into view once it's generated.

## Challenges Overcome

The biggest challenge was ensuring the ingredient list updated correctly before sending the request to the AI. Since React state updates are asynchronous, I learned how to structure my logic to use the most up-to-date data, ensuring the AI always receives the full list of ingredients.
