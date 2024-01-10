<script>
  let map;
  let L;
  import { onMount } from "svelte";
  import "leaflet/dist/leaflet.css";

  onMount(async () => {
    L = await import("leaflet");
    map = L.map("map").setView([51.505, -0.09], 13);
    L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {}).addTo(
      map,
    );
    map.attributionControl.setPrefix("github.com/anzhi0708");
  });
</script>

<h1>Welcome to SvelteKit</h1>
<div id="map" />
<p>
  Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
</p>

<style>
  #map {
    height: 360px;
  }
</style>
