<template>
  <div>
    <h2>JSONPlaceholder API Demo</h2>

    <div v-if="loading">Loading...</div>
    <div v-if="error">{{ error }}</div>

    <h3>Posts</h3>
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{ post.title }} (ID: {{ post.id }})
        <button @click="editPost(post)">Edit</button>
        <button @click="deletePost(post.id)">Delete</button>
      </li>
    </ul>

    <h3>Add New Post</h3>
    <form @submit.prevent="addPost">
      <!-- Added self-closing slashes below -->
      <input type="text" v-model="newPost.title" placeholder="Title" required />
      <br />
      <textarea v-model="newPost.body" placeholder="Body" required></textarea>
      <br />
      <button type="submit">Add Post</button>
    </form>

    <div v-if="editingPost">
      <h3>Edit Post</h3>
      <form @submit.prevent="updatePost">
        <!-- Added self-closing slashes below -->
        <input type="text" v-model="editPostData.title" placeholder="Title" required />
        <br />
        <textarea v-model="editPostData.body" placeholder="Body" required></textarea>
        <br />
        <button type="submit">Update Post</button>
        <button @click="cancelEdit">Cancel</button>
      </form>
    </div>
  </div>
</template>
