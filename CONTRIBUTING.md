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
/* Add any necessary Astro frontmatter logic here */
---

<section class="flex items-center justify-center">
    <div class="loader">
        <!-- Your loader code goes here -->
    </div>
</section>

<style>
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
