<script lang="ts">
  import { feedback } from "../stores";

  $: count = $feedback.length;
  $: average =
    $feedback.reduce((curr, { rating }) => curr + rating, 0) / $feedback.length;
</script>

<div class="feedback-stats">
  <h4>{count} Reviews</h4>
  <h4>Ratings Average: {average}</h4>
</div>

<style>
  .feedback-stats {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>
