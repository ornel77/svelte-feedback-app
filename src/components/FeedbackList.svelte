<script>
  // import {onMount, onDestroy} from 'svelte'
  import {FeedbackStore} from '../stores'
  import { fade, scale } from "svelte/transition";
  import FeedbackItem from "./FeedbackItem.svelte";

  // // to get the data from the store, the longer way :
  // let feedback = [];

  // const unsubscribe = FeedbackStore.subscribe((data) => feedback = data)

  // onDestroy(() => {
  //   unsubscribe()
  // })


</script>

{#each $FeedbackStore as fb (fb.id)}
  <div in:scale out:fade={{ duration: 500 }}>
    <FeedbackItem item={fb} />
  </div>
{/each}
