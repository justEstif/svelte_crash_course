<script lang="ts">
  import FeedbackItem from "./FeedbackItem.svelte";
  import { feedback } from "../stores";
</script>

<ul>
  {#each $feedback as fb}
    <FeedbackItem item={fb} />
  {/each}
</ul>
