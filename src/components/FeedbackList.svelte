<script>
  import FeedbackItem from "./FeedbackItem.svelte";
  import { fade, scale } from "svelte/transition";
  import { FeedbackStore } from "../stores";

  </script>

{#each $FeedbackStore as fb (fb.id)}
  <div in:scale out:fade={{ duration: 500 }}>
    <FeedbackItem item={fb} />
  </div>
{/each}
