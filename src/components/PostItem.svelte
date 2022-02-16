<script>
  export let title
  export let content
</script>

<div class="post">
  <h4>{title || 'Example'}</h4>
  <p>{content || 'I am a litte post!'}</p>
</div>

<style>
  .post {
    background-color: burlywood;
    color: brown;
    width: 20rem;
    height: max-content;
    padding: 1.5rem;
    border-radius: .5rem;
  }
</style>