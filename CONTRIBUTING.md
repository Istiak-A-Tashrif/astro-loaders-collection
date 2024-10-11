# Contribution Guide

## Goal
The goal is to create a collection of ready-to-use loaders built with Astro and styled using Tailwind CSS for easy implementation.

## Code

1. Add your new component in `/src/components/`. Make sure to use appropriate name and path.
2. Prefer using Tailwind CSS for styling. You can still use plain CSS if you prefer.
3. Please keep the naming conventions as `loader-[your github username]-[number].astro` ex. `loader-gaurav_bhalerao-01.astro`.

## Issues

1. Before creating an issue, check if someone has already worked on the similar loader you want to create. You can still recreate the component if you want, but make sure the design is not too similar.
2. Create an issue with the component name.
3. Create a branch attached to that issue.

## Pull Requests
1. After you complete your design, create a pull request.
2. Check if there are any conflicts, If yes, then please solve them and push to same branch.

## Component Template
```
---
const author = "Gaurav Bhalerao"
const github = "https://github.com/gaurav-bhalerao-107"
---

<section class="relative flex items-center justify-center h-full w-full">
  <!-- Loader -->
  <div class="loader h-full w-full flex justify-center items-center">
    <!-- Your loader code goes here -->
  </div>

  <!-- Author Details -->
  <div class="absolute bottom-0 right-0 text-right">
    <h2 class="text-xs font-medium tracking-wider leading-3">{ author }</h2>
    <a href={github} class="text-[10px] tracking-wider text-blue-500" target="_blank">GitHub Profile</a>
  </div>
</section>

<style scoped>
/* Add any custom styles here if necessary */
.loader {
    /* Custom styles for loader animation */
}
</style>

<script>
  // Add your JavaScript for the loader if needed
  // This script will be scoped to this component
</script>
```

## Component Example
```
---
const author = "Gaurav Bhalerao"
const github = "https://github.com/gaurav-bhalerao-107"
---

<section class="relative flex items-center justify-center h-full w-full">
  <!-- Loader -->
  <div class="loader h-full w-full flex justify-center items-center">
    <div class="loading pacifico-regular" data-text="loading...">Loading...</div>
  </div>

  <!-- Author Details -->
  <div class="absolute bottom-0 right-0 text-right">
    <h2 class="text-xs font-medium tracking-wider leading-3">{ author }</h2>
    <a href={github} class="text-[10px] tracking-wider text-blue-500" target="_blank">GitHub Profile</a>
  </div>
</section>

<style scoped>
.loader .loading {
  position:absolute;
  font-size:26px;
  color:white;
  text-transform:uppercase;
  letter-spacing:5px;
  border-bottom:16px solid white;
}

.loader .loading:before {
  content: attr(data-text);
  position:absolute;
  color:cyan;
  overflow:hidden;
  border-bottom:16px solid cyan;
  animation: slide 4.5s linear infinite;
}

@keyframes slide {
  0% { width:0; }
      
  100%{ width:100%; }
}
</style>

<script>
  
</script>
```