<script>
  let title = ''
  let content = ''
  export let onSubmit
  const handleSubmit = () => {
    onSubmit({title, content})
    title = ""
    content = ""
  }

</script>

<form on:submit|preventDefault={handleSubmit}>
  <h2>Create your post</h2>
  <label for="title">Title</label>
        <input
          id="title"
          type="text"
          name="title"
          bind:value={title}
          onChange={(e) => title = e.target.value}
        />
        <label for="content">Content</label>
        <textarea
          id="content"
          name="content"
          bind:value={content}
          rows={4}
          onChange={(e) => content = e.target.value}
        />

        <button type="submit">Post</button>
</form>

<style>
  form {
    display: flex;
    flex-direction: column;
    max-width: 20rem;
    border-radius: .5rem;
    background-color: brown;
    color: white;
    padding: 1.5rem;
    margin: 1rem;
    height: fit-content;
  }
  button {
    background-color: chocolate;
    border: none;
    cursor: pointer;
    color: white;
    font-weight: bold;
  }
</style>