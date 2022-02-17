<script>
  import PostForm from './PostForm.svelte';
  import PostItem from './PostItem.svelte'

  $: posts = []

  const saveNewPost = (post) => {
    posts = [post,...posts]
  }
</script>

<div class="container">
  <PostForm onSubmit={saveNewPost}/>
  <div class="post-container">
    
    {#if posts.length === 0}
    <PostItem />
    {/if}
    
    {#each posts as post}
    <PostItem title={post.title} content={post.content}/>
    {/each}
  </div>
</div>

<style>
  .container {
    background-color: antiquewhite;
    padding: 2rem;
  }

  .post-container {
    display: flex;
    flex-wrap: wrap;
    gap: .5rem;
    margin: auto;
    max-width: 75%;
    padding: 2rem;

  }
</style>