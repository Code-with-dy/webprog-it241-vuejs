<template>
  <div id="app">
    <h1>My Personal Profile Web page - Dylan D. Villanueva</h1>
    <p>
      About Me<br />
      <h1>My Personal Profile Web page</h1>
      <p>
        About Me<br />
        My name is Dylan D. Villanueva<br />
        I am 19 years old<br />
        Currently living at San Antonio Village Makati City<br />
        I am currently studying at Asia Pacific College<br />
        My Course is Bachelor of Science In Information Technology<br />
        My Hobbies are playing mobile games, watching anime, Playing different kinds of sports and I like to Travel in different areas<br />
      </p>
    </p>

    <!-- Note: The image source URL was incomplete in your HTML snippet, I've closed the tag here. 
         You may need to fix the URL to display the image correctly. -->
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQy31gH8mAAkJ57L0g-H_k-7o4CCaUD_pidbQ&s" />

    <div class="container">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
      <div>7</div>
      <div>8</div>
      <div>9</div>
      <div>10</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  // You would add data, methods, or components here if needed for interactivity.
};
</script>

<style>
/* You would copy the contents of your 'css/flexbox.css' file into this style block */
.container {
  display: flex; /* Example CSS from flexbox.css */
  flex-wrap: wrap;
  gap: 10px;
}
.container div {
  background-color: #f1f1f1;
  padding: 20px;
  text-align: center;
  /* Add other flexbox styles here */
}
</style>
