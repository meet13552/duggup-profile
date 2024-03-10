<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import Profile from "$lib/components/Profile.svelte";
  import Timeline from "$lib/components/Timeline.svelte";
import "../app.pcss";
import jsonData from '../data.json';
</script>
<Header />
<Profile {jsonData}/>
<Timeline {jsonData}/>
<slot />