# Authentication Refactor and UX Improvements

## Goals
- Evaluate developer’s understanding of Vue 3, Vuex, and related best practices.
- Assess coding style, problem-solving approach, and submission quality.
- Ensure implementation without external AI tools.

## Tasks

- [ ] **Signup & Signin Error Handling**
  - Replace notification-only error handling with inline validation messages under input fields.
  - Validate input before making API calls (e.g., invalid email, empty password).
  - Errors should be reactive and displayed directly below the corresponding input.

- [ ] **Move Authentication Logic to Vuex**
  - Create a dedicated `auth` Vuex module.
  - Implement actions for `login` and `signup`.
  - Manage state for `user`, `token`, `loading`, and `errors`.
  - Components should only dispatch actions and consume state, not handle API logic directly.

- [ ] **Display User Info on Homepage**
  - After successful login, update Vuex `user` state with user data from the API response.
  - Show logged-in user’s details (e.g., name, email) on the homepage.

## Acceptance Criteria
- Inline error messages appear under inputs for invalid signup/signin attempts.
- All authentication logic is centralized in Vuex store.
- User information is displayed on the homepage after login.
- Code follows Vue 3 and Vuex best practices with clean and consistent style.

## Deadline
- 4 hours from assignment.
