<script>
  import FeedbackForm from './components/FeedbackForm.svelte';
  import FeedbackList from './components/FeedbackList.svelte';
  import FeedbackStats from './components/FeedbackStats.svelte';
  

  // const deleteFeedback = (e) => {
  //   const itemId = e.detail;
  //   feedback = feedback.filter((item) => item.id !== itemId);
  // };

  // const addFeedback = e => {
  //   const newFeedback = e.detail
  //   console.log(newFeedback)
  //   feedback = [newFeedback, ...feedback, ]
  // }
</script>

<main class="container">
  <FeedbackForm />
  <FeedbackStats />
  <FeedbackList />
</main>
