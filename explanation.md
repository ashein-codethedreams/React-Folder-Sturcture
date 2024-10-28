## Explanation of Each Directory

### `public/`

Contains static files served directly by the server. The `index.html` file is the root HTML for the app, and the `assets/` folder holds images, fonts, etc.

### `src/`

Main source code directory for all app logic and components.

- #### `api/`

  - **`apiSlice.js`**: Sets up RTK Query with the base API configuration.
  - **`authApiSlice.js`**: Defines authentication-related API calls, such as login and register.

- #### `app/`

  - **`store.js`**: Configures the Redux store and includes RTK Query and Redux slices for app-wide state management.

- #### `components/`

  Contains reusable UI components, such as buttons and inputs, for styling consistency and reusability.

- #### `features/`

  Contains feature-based modules. Each module has Redux logic, components, and any other logic required for that feature.

  - **`auth/`**
    - **`AuthSlice.js`**: Redux slice to manage the authentication state.
    - **`LoginForm.js`**: Form component that handles login actions.
    - **`ProtectedRoute.js`**: Route wrapper component to protect pages that require authentication.

- #### `hooks/`

  Holds custom hooks to centralize logic that’s reused across components.

  - **`useAuth.js`**: Provides authentication status and checks.

- #### `pages/`
  Full-page components for main views (e.g., Home, Login) that serve as top-level UI screens.
