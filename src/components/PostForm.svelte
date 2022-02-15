<script>
  let title = ''
  let content = ''
  const handleSubmit = () => {

  }
</script>

<form on:submit|preventDefault={handleSubmit}>
  <h2>Create your post</h2>
  <label for="title">Title</label>
        <input
          id="title"
          type="text"
          name="title"
          value={title}
          onChange={(e) => title = e.target.value}
        />
        <label for="content">Content</label>
        <textarea
          id="content"
          name="content"
          value={content}
          rows={4}
          onChange={(e) => content = e.target.value}
        />

        <button type="submit">Save</button>
</form>