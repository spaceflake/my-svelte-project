<script>
  import Hero from "./Hero.svelte";
  import PostForm from './PostForm.svelte';

  const posts = []

  const saveNewPost = (post) => {
    posts = [post,...posts]
  }
</script>
<Hero />
<PostForm on:submit={saveNewPost}/>