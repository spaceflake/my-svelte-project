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
    --shadow-color: 35deg 29% 57%;
    background-color: burlywood;
    color: brown;
    max-width: 20rem;
    min-width: 10rem;
    /* height: max-content; */
    padding: 1.5rem;
    border-radius: .5rem;
    border: 1px solid brown;
    box-shadow: 0.3px 0.5px 0.7px hsl(var(--shadow-color) / 0.36),
    0.8px 1.6px 2px -0.8px hsl(var(--shadow-color) / 0.36),
    2.1px 4.1px 5.2px -1.7px hsl(var(--shadow-color) / 0.36),
    5px 10px 12.6px -2.5px hsl(var(--shadow-color) / 0.36);;
  }
  h4, p {
    margin-top: 0;
  }
</style>