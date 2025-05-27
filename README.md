# Repo Explorer

## Goal
The goal of this assignment is to assess your ability to build a well-structured, performant, and user-friendly React Native application using modern best practices, including the new bridgeless architecture and Gluestack UI.

## Project Description
You are tasked with building a "GitHub Repo Explorer" application. This app will allow users to search for public GitHub repositories and view some basic details about them.

## Core Requirements

1.  **Technology Stack:**
    *   **React Native:** Latest stable version.
        *   **Bridgeless Architecture (New Architecture):** Your project **must** be configured to use the New Architecture (Fabric enabled for UI, TurboModules for native modules).
            *   Android: `newArchEnabled=true` in `android/gradle.properties`.
            *   iOS: Ensure `RCT_NEW_ARCH_ENABLED=1` is set (usually handled by `npx react-native-new-architecture enable` or manual setup during `pod install`).
    *   **Gluestack UI:** All UI components must be implemented using `@gluestack-ui/themed` and `@gluestack-style/react`.
    *   **Language:** TypeScript.
    *   **State Management:** Choose a state management solution you deem appropriate (e.g., React Context, Zustand, Redux Toolkit). Justify your choice in the README.
    *   **API:** GitHub Public API (e.g., `https://api.github.com/search/repositories?q={query}`). No authentication is required for public repo search.

2.  **Screens & Functionality:**
    *   **Search Screen:**
        *   An input field (using Gluestack `Input`) for users to type their search query (e.g., "react native", "gluestack").
        *   A search button (using Gluestack `Button`).
        *   Upon pressing the search button, fetch repositories from the GitHub API based on the query.
        *   Display a loading indicator (e.g., Gluestack `Spinner`) while data is being fetched.
        *   Display search results in a scrollable list (e.g., using Gluestack `FlatList` or a custom component built with Gluestack primitives suitable for virtualized lists).
        *   Each list item should display:
            *   Repository Name
            *   Owner's Login
            *   Star Count
            *   A brief description
        *   Handle empty states (no results found) and error states (API errors, network issues) gracefully using appropriate Gluestack components (e.g., `Text`, `Heading`, `Box` for layout).
        *   Tapping on a list item should navigate the user to the Detail Screen.
    *   **Detail Screen:**
        *   Display more detailed information about the selected repository:
            *   Repository Name (as a `Heading`)
            *   Owner's Login
            *   Star Count
            *   Fork Count
            *   Number of Open Issues
            *   Primary Language
            *   Full Description
            *   Link to the repository on GitHub (make this a tappable Gluestack `Link` that opens in the device browser).
        *   A "Back" button or header navigation to return to the Search Screen.

3.  **Code Quality & Structure:**
    *   Clear, well-organized, and maintainable code.
    *   Reusable components where appropriate.
    *   Proper error handling and user feedback.
    *   Follow TypeScript best practices.
    *   Directory structure that makes sense for a growing application.

4.  **Testing:**
    *   Write basic unit tests for at least one key component or utility function using a testing framework like Jest and React Native Testing Library.

## Bonus Requirements (Optional, but will be looked upon favorably):

*   **Debouncing:** Implement debouncing for the search input to avoid excessive API calls.
*   **Pagination/Infinite Scroll:** For the search results list.
*   **Theming:** Demonstrate minor custom theming with Gluestack (e.g., changing primary color or font styles).
*   **Accessibility:** Ensure basic accessibility best practices are followed (e.g., proper `accessibilityLabel`s on interactive elements).
*   **Caching:** Simple caching strategy for API responses (e.g., in-memory for a short duration).
*   **Advanced State Management:** If you choose a more complex state management library, demonstrate its benefits clearly.

## Evaluation Criteria

Your submission will be evaluated based on:

1.  **Correctness & Functionality:** Does the app meet all core requirements and function as expected?
2.  **Code Quality & Structure:** Is the code clean, readable, maintainable, and well-organized?
3.  **React Native New Architecture:** Is the project correctly set up for the New Architecture? Is there an understanding of its principles?
4.  **Gluestack UI Implementation:** Effective and appropriate use of Gluestack components and styling.
5.  **State Management:** Sensible choice and implementation of a state management solution.
6.  **API Integration:** Clean and robust API integration with proper loading and error handling.
7.  **Testing:** Quality and relevance of unit tests.
8.  **Git Usage:** Clear commit history.
9.  **Documentation:** A comprehensive README file (this file!).
10. **Problem Solving:** How you approach challenges and make technical decisions.

## Submission Guidelines

1.  Initialize a Git repository for your project.
2.  Commit your changes frequently with clear and descriptive messages.
3.  Push your repository to a public Git hosting service (e.g., GitHub, GitLab).
4.  Ensure this `README.md` file is comprehensive and includes:
    *   **Setup Instructions:** Detailed instructions on how to clone, install dependencies, and run the project on both iOS and Android. Include any specific environment setup if needed (e.g., Node version, Watchman, specific JDK, Xcode version).
    *   **Architectural Choices:** A brief explanation of your architectural decisions, especially regarding state management (why you chose it) and any significant structural patterns used.
    *   **Assumptions Made:** List any assumptions you made during development.
    *   **Challenges Faced:** Describe any challenges encountered and how you overcame them.
    *   **Requirements Met:** Clearly list which core requirements you've met.
    *   **Bonus Requirements Attempted/Met:** List any bonus requirements you attempted and/or completed.
    *   **Time Spent:** An estimate of the time you spent on the assignment.
5.  Submit the link to your public repository.

## A Note on the New Architecture
The primary focus for the New Architecture requirement is on correctly setting up an RN project with Fabric enabled and understanding its implications. You are not expected to write complex custom Fabric components or TurboModules unless you identify a specific need and have the time to demonstrate that skill. Your React component structure and state management choices should ideally reflect an awareness of the potential performance benefits and direct communication capabilities offered by Fabric.
