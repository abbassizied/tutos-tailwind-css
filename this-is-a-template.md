# html template

```html
<!DOCTYPE html>
<html>
<head>
<title> XXXX </title>
<style>


</style>
<link rel="stylesheet" href="./proj-xx/style.css">
<script src="./proj-xx/script.js"></script>
</head>
<body>

<h1> Nothing Found - This is a template.</h1>

<!--
Set of minimal, reusable Tailwind CSS code snippets for common UI components
-->

<!-- Main Container 
- container: Limits width to screen breakpoints.
- mx-auto: Centers the container.
- p-4: Adds padding
-->
<div class="container mx-auto p-4">
  <!-- Content here -->

<!-- Navigation Bar 
- flex, items-center, justify-between: Aligns items.
- hover:underline: Adds interactivity
-->
<nav class="flex items-center justify-between p-4 bg-gray-800 text-white">
  <div class="text-xl font-bold">MyApp</div>
  <ul class="flex space-x-4">
    <li><a href="#" class="hover:underline">Home</a></li>
    <li><a href="#" class="hover:underline">About</a></li>
  </ul>
</nav>


<!-- Pagination 
- space-x-2: Spacing between buttons.
- bg-blue-500: Highlights the active page 
-->
<div class="flex space-x-2 p-2 bg-gray-100 rounded">
  <button class="px-3 py-1 bg-blue-500 text-white rounded">Previous</button>
  <button class="px-3 py-1 hover:bg-gray-200 rounded">1</button>
  <button class="px-3 py-1 bg-blue-500 text-white rounded">2</button>
  <button class="px-3 py-1 hover:bg-gray-200 rounded">3</button>
  <button class="px-3 py-1 hover:bg-gray-200 rounded">Next</button>
</div>

<!-- Table 
- divide-y: Adds borders between rows.
- hover:bg-gray-50: Highlights rows on hover
-->
<table class="min-w-full divide-y divide-gray-200">
  <thead class="bg-gray-50">
    <tr>
      <th class="px-6 py-3 text-left">ID</th>
      <th class="px-6 py-3 text-left">Name</th>
    </tr>
  </thead>
  <tbody class="divide-y divide-gray-200">
    <tr class="hover:bg-gray-50">
      <td class="px-6 py-4">1</td>
      <td class="px-6 py-4">John Doe</td>
    </tr>
  </tbody>
</table>

<!-- Buttons 
- bg-*/500: Default color.
- hover:bg-*/600: Darkens on hover
-->
<button class="px-4 py-2 bg-blue-500 text-white font-semibold rounded hover:bg-blue-600">
  Submit
</button>

<button class="px-4 py-2 bg-gray-300 text-gray-700 font-semibold rounded hover:bg-gray-400">
  Cancel
</button>

<!-- Alert/Notification 
- bg-yellow-100: Subtle background.
- hover:text-yellow-900: Darkens close button on hover
-->
<div class="p-4 rounded bg-yellow-100 text-yellow-800 mb-4">
  <button class="float-right ml-2 hover:text-yellow-900">× Close</button>
  <p>This is an alert message.</p>
</div>


</div>


</body>
</html>
```
