<script lang="ts">
  import type { IFeedbackitem } from "../types";
  import FeedbackItem from "./FeedbackItem.svelte";
  export let feedback: IFeedbackitem[] = [];
</script>

<ul>
  {#each feedback as fb}
    <FeedbackItem item={fb} />
  {/each}
</ul>
