# Lesson 3 -Introduction to Single Page Routing With ui-router

Alternative implementation of single page architecture with modular component architecture and service architecture demonstrating asynchronous multi-threading.

Example 37 demonstrates state transition while asynchronous processes are still unresolved. you'll see a slight delay in the presentation of the shopping list data to demontrate this.

This example (38) is an alternative in which ui-router will wait for resolution of the "promise" before transitioning to the new state. the key difference is this snippet in routes.js

resolve: {
items: ['ShoppingListService', function (ShoppingListService) {
return ShoppingListService.getItems();
}]


Example Site:  https://lpm0073.github.io/jhu-course5-module3-lecture38/

Lecture:
https://www.coursera.org/learn/single-page-web-apps-with-angularjs/lecture/OupEk/lecture-38-part-2-routing-state-with-resolve
