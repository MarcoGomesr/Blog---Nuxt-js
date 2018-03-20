<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnailImage="post.thumbnailImage"
      :id="post.id"
     />
  </section>
</template>

<script>

import PostPreview from '@/components/Blog/PostPreview'

export default {
  components: {
   PostPreview 
  },

  data(){
   return {
     posts: [
       { title: 'A new Begining', previewText: 'This will be awesome, Don\t miss it', thumbnailImage: 'http://via.placeholder.com/350x150', id: "a-new-begining" },
       { title: 'A second Begining', previewText: 'This will be awesome, Don\t miss it again', thumbnailImage: 'http://via.placeholder.com/350x150', id: "a-second-begining" }
     ]
   }
 }
}
</script>

<style>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
@media(min-width: 35rem){
  #posts {
    flex-direction: row;
  }
}
</style>