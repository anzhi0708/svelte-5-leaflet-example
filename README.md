# Svelte 5 - Leaflet.js Example
An Example of Drawing a Map with Svelte + Leaflet

## Key Points

- You need to place the `map`'s initialization in the `onMount` hook to ensure that `Leaflet` is rendered on the client side, not the server side.

- Also, you need to import the `leaflet/dist/leaflet.css` file and specify the element's `height` in the `<style>` block in order for the map to display correctly.
