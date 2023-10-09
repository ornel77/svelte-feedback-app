<script>
  import { FeedbackStore } from "../stores";

  $: count = $FeedbackStore.length;
  $: average =
    $FeedbackStore.reduce((p, { rating }) => p + rating, 0) / $FeedbackStore.length || 0;


</script>

<div class="feedback-stats">
  <h4>{count} {count === 1 ? "review" : "reviews"}</h4>
  <h4>Rating average: {average.toFixed(1)}</h4>
</div>

<style>
  .feedback-stats {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>
