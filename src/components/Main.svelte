<script>
  import Hero from "./Hero.svelte";
  import PostForm from './PostForm.svelte';
  import PostItem from './PostItem.svelte'

  $: posts = []

  const saveNewPost = (post) => {
    posts = [post,...posts]
  }
</script>
<Hero />
<div class="container">
  <PostForm onSubmit={saveNewPost}/>
  <div class="post-container">
    <PostItem />
    
    {#each posts as post}
    <PostItem title={post.title} content={post.content}/>
    {/each}


  </div>
</div>

<style>
  .container {
    display: flex;
    background-color: antiquewhite;
    padding: 2rem;
  }

  .post-container {
    display: flex;
    flex-wrap: wrap;
    gap: .5rem;
    margin: 1rem;
  }
</style>