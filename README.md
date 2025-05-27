# Movie Buff

## Goal
To evaluate your proficiency in building a polished, high-performing, and intuitive React Native application utilizing the latest bridgeless architecture, Gluestack UI, and best practices in frontend development.

## Project Description
You will create "Movie Buff," an application that allows users to discover popular movies, search for specific titles, and view their details.

## Core Requirements

1.  **Technology Stack:**
    *   **React Native:** Latest stable version.
        *   **Bridgeless Architecture (New Architecture):** Your project **must** be configured to use the New Architecture (Fabric enabled for UI, TurboModules for native modules).
            *   Android: `newArchEnabled=true` in `android/gradle.properties`.
            *   iOS: Ensure `RCT_NEW_ARCH_ENABLED=1` is set (usually handled by `npx react-native-new-architecture enable` or manual setup during `pod install`).
    *   **Gluestack UI:** All UI components must be implemented using `@gluestack-ui/themed` and `@gluestack-style/react`.
    *   **Language:** TypeScript.
    *   **State Management:** Select a state management library or pattern you feel is suitable for this application's scale (e.g., React Context, Zustand, Redux Toolkit). Justify your selection in the README.
    *   **API:** The Movie Database (TMDB) API. You'll need to register for a free API key. (e.g., endpoints for popular movies, search, movie details). *Ensure your API key is not hardcoded directly in the committed code; use environment variables or a similar secure method.*

2.  **Screens & Functionality:**
    *   **Discover Screen (Initial Screen):**
        *   Display a list of currently popular or trending movies fetched from TMDB.
        *   Each movie in the list should display (at a minimum):
            *   Poster image (using Gluestack `Image`).
            *   Title (using Gluestack `Heading` or `Text`).
            *   Release Date or Popularity Score.
        *   The list should be scrollable (e.g., Gluestack `FlatList` or a custom virtualized list built with Gluestack primitives).
        *   Implement a loading state (e.g., Gluestack `Spinner`) while fetching data.
        *   Handle API errors and empty states gracefully.
        *   Tapping a movie item navigates to the Movie Detail Screen.
    *   **Search Functionality:**
        *   Include an input field (Gluestack `Input`) allowing users to search for movies by title. This can be on the Discover screen or a separate Search screen/tab.
        *   As the user types (or upon submission), fetch and display search results in a similar list format to the Discover screen.
        *   Handle loading, error, and "no results" states.
    *   **Movie Detail Screen:**
        *   Display detailed information for a selected movie:
            *   Large Poster Image
            *   Title (Gluestack `Heading`)
            *   Overview/Synopsis (Gluestack `Text`)
            *   Release Date
            *   Average Rating / Vote Count
            *   Genres (if available from API)
        *   Provide a "Back" button or header navigation to return to the previous screen.

3.  **Code Quality & Structure:**
    *   Well-structured, clean, and maintainable code.
    *   Create reusable components where logical (e.g., MovieListItem).
    *   Implement robust error handling and provide clear user feedback.
    *   Adhere to TypeScript best practices.
    *   Organize your project with a sensible directory structure.

4.  **Testing:**
    *   Write basic unit tests for at least one significant component or utility function (e.g., an API service function, a complex UI component) using Jest and React Native Testing Library.

## Bonus Requirements (Optional, but highly valued):

*   **Favorites System:**
    *   Allow users to mark movies as "favorites" (e.g., an icon button on list items and the detail screen).
    *   Persist these favorites locally (e.g., using AsyncStorage or a simple local DB solution).
    *   Add a "Favorites" screen/tab to display all favorited movies.
*   **Debounced Search:** Implement debouncing on the search input to optimize API calls.
*   **Pagination/Infinite Scroll:** For the Discover and/or Search results.
*   **Custom Gluestack Theming:** Showcase minor theme customizations (e.g., adjusting primary colors, component variants, or font styles).
*   **Advanced Error Handling:** More specific error messages or user guidance for different API/network issues.
*   **Pull-to-Refresh:** On the Discover screen to refresh the list of popular movies.

## Evaluation Criteria

Your submission will be judged on:

1.  **Functionality & Correctness:** Does the application meet all core requirements and operate as expected?
2.  **Code Quality & Organization:** Is the codebase clean, readable, logically structured, and maintainable?
3.  **React Native New Architecture Implementation:** Is the project correctly configured for the New Architecture and demonstrates an understanding of its concepts?
4.  **Gluestack UI Usage:** Proficient and appropriate use of Gluestack components and styling capabilities.
5.  **State Management:** Rational choice and effective implementation of the chosen state management approach.
6.  **API Interaction:** Clean, efficient, and resilient integration with the TMDB API, including proper handling of loading states and errors.
7.  **Testing:** Meaningful and well-written unit tests.
8.  **Git Practices:** Clear, atomic commits with descriptive messages.
9.  **Documentation:** A well-written and informative README file (this file!).
10. **Problem-Solving Skills:** Your approach to tackling challenges and making sound technical decisions.

## Submission Guidelines

1.  Initialize a Git repository for your project.
2.  Make frequent commits with clear, descriptive messages.
3.  Host your repository on a public Git platform (e.g., GitHub, GitLab).
4.  Ensure this `README.md` file is comprehensive and includes:
    *   **API Key Setup:** Clear instructions on how to get an API key from TMDB and configure it for the project (e.g., via an environment variable file that's gitignored, such as `.env`).
    *   **Setup Instructions:** Detailed steps for setting up the development environment, installing dependencies, and running the application on both iOS and Android. Include any specific environment setup if needed (e.g., Node version, Watchman, specific JDK, Xcode version).
    *   **Architectural Choices:** A brief overview of your architectural decisions, especially regarding state management (why you chose it) and any significant structural patterns used.
    *   **Assumptions Made:** List any assumptions you made during development.
    *   **Challenges Faced:** Describe any challenges encountered and how you overcame them.
    *   **Requirements Met:** Clearly list which core requirements you've met.
    *   **Bonus Requirements Attempted/Met:** List any bonus requirements you attempted and/or completed.
    *   **Time Spent:** An estimate of the time you spent on the assignment.
5.  Submit the link to your public repository.

## Time Expectation
We anticipate this assignment will require approximately 4-8 hours of focused effort. Please prioritize quality and demonstrating your core skills within this timeframe.

## A Note on the New Architecture
The main expectation regarding the New Architecture is its correct setup and your ability to develop within this environment. Writing custom, complex Fabric components or TurboModules is not required unless you find it essential for a specific feature and wish to showcase this advanced skill (time permitting). Your component design and state management should, however, be developed with an understanding of the new architecture's benefits.

---

Good luck, and we're excited to see what you build!