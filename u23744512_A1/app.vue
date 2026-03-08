<template>
  <!--Miguel De Freitas u23744512-->
  <div>
  <nav>
   <NuxtLink to="/">Home</NuxtLink>
   <NuxtLink to="/projects">Projects</NuxtLink>
   <NuxtLink to="/contact">Contact</NuxtLink>
   </nav>
   <NuxtPage/>
  </div>
</template>
<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  max-width: 850px;
  margin: 0 auto;
  padding: 2rem;
  background: #f0f4f8;
  color: #333;
}

nav {
  background: #2c3e50;
  padding: 1rem 2rem;
  border-radius: 8px;
  margin-bottom: 2rem;
}

nav a {
  margin-right: 1.5rem;
  text-decoration: none;
  color: #ecf0f1;
  font-weight: bold;
  font-size: 1rem;
}

nav a:hover {
  color: #3498db;
}

section {
  background: white;
  border-radius: 8px;
  padding: 1.5rem 2rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
  border-left: 5px solid #3498db;
}

h1 {
  color: #2c3e50;
  margin-bottom: 0.75rem;
  font-size: 2rem;
}

h2 {
  color: #2980b9;
  margin-bottom: 0.75rem;
  font-size: 1.3rem;
}

p {
  line-height: 1.7;
  color: #555;
}

.project-card {
  background: #eaf4fb;
  border: 1px solid #aed6f1;
  border-radius: 6px;
  padding: 1rem 1.5rem;
  margin-bottom: 1rem;
}

.project-card h3 {
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

input, textarea {
  display: block;
  width: 100%;
  margin-bottom: 1rem;
  padding: 0.6rem 0.8rem;
  font-size: 1rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  background: #fafafa;
}

input:focus, textarea:focus {
  outline: none;
  border-color: #3498db;
  background: white;
}

label {
  display: block;
  margin-bottom: 0.3rem;
  font-weight: bold;
  color: #2c3e50;
}

button {
  padding: 0.6rem 1.75rem;
  background: #3498db;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 1rem;
}

button:hover {
  background: #2980b9;
}
</style>