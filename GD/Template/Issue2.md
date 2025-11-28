
# 📌 React Developer Technical Test – *Image Gallery*

### **Context / Idea**

Build a small **Image Gallery** app that loads images from a public API (e.g., [Unsplash API](https://unsplash.com/developers) or [Picsum Photos](https://picsum.photos/)), supports infinite scrolling, and allows users to "favorite" images.

---

## **Part 1 – Custom React Hook**

**Problem:**
Create a custom React Hook called `useFetchImages` that:

* Accepts `page` and `limit` as arguments.
* Fetches images from the API.
* Returns `{ images, loading, error }`.

👉 **Test Evaluation**

* Correct use of `useEffect` and `useState`.
* Error handling.
* Hook reusability (should work for other API endpoints).

## **Part 2 – Redux Toolkit**

**Problem:**
Integrate **Redux Toolkit** for managing **favorite images**.

Requirements:

* A slice called `favoritesSlice`.
* State: `{ favorites: [] }`.
* Reducers: `addFavorite(image)`, `removeFavorite(imageId)`.
* Selector: `selectFavorites`.

👉 **Test Evaluation**

* Proper use of Redux Toolkit (`createSlice`, `configureStore`).
* Correct handling of immutability.
* Using `useSelector` + `useDispatch` in components.

## **Part 3 – Lazy Loading with Infinite Scroll**

**Problem:**
Implement **infinite scroll** for loading images:

* As the user scrolls near the bottom, load the next page of images using `useFetchImages`.
* Show a loading spinner when fetching new images.

👉 **Test Evaluation**

* Usage of Intersection Observer API or scroll event listener.
* Preventing duplicate API calls.
* Smooth UI updates without blocking.

## **Part 4 – Avoiding Unnecessary Re-renders**

**Problem:**
Optimize the gallery:

* The `ImageCard` component should only re-render when its own props change.
* Use `React.memo`, `useCallback`, and `useMemo` where appropriate.
* Ensure adding/removing favorites does not re-render unrelated images.
