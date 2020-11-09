# CustomerApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.1.1.

## This project introduces the new syntax used for lazy loading of feature modules in Angular V7 and above

1. Ref: <https://angular.io/guide/lazy-loading-ngmodules#lazy-loading-feature-modules>
2. Ref: <https://stackoverflow.com/questions/56748335/angular-8-lazy-loading-syntax-not-working>
3. Ref: <https://ultimatecourses.com/blog/lazy-load-angular-modules>
4. Run ```ng new customer-app --routing```
5. Run ```ng generate module customers --route customers --module app.module```

### Task: Add customer files

### Task: Add another feature module (orders)

1. Run```ng generate module orders --route orders --module app.module```

### Task: Set up the UI

1. Ref <https://angular.io/guide/lazy-loading-ngmodules#set-up-the-ui>

```html

<!-- app.component.html -->

<h1>
  {{title}}
</h1>

<button routerLink="/customers">Customers</button>
<button routerLink="/orders">Orders</button>
<button routerLink="">Home</button>

<router-outlet></router-outlet>

```

![Landing page](/src/app/images/ui.jpg)

- The landing page

### Task: Imports and route configuration

1. Ref: <https://angular.io/guide/lazy-loading-ngmodules#imports-and-route-configuration>

### Task: Inside the feature module

1. Ref: <https://angular.io/guide/lazy-loading-ngmodules#inside-the-feature-module>

### Task: Verify lazy loading

1. Ref: <https://angular.io/guide/lazy-loading-ngmodules#verify-lazy-loading>

![Orders page](/src/app/images/orders.jpg)

![Customers page](/src/app/images/customers.jpg)

1. forRoot() and forChild()
2. Ref: <https://angular.io/guide/lazy-loading-ngmodules#forroot-and-forchild>

NOTE:

1. Use ```RouterModule.forRoot()``` only once in the application, inside the **AppRoutingModule**.
2. The CLI also adds ```RouterModule.forChild(routes)``` to feature routing modules
3. You can use ```forChild()``` in multiple modules.
4. The ```forRoot()``` method takes care of the global injector configuration for the Router.
5. The ```forChild()``` method has no injector configuration. It uses directives such as ```RouterOutlet``` and ```RouterLink```.
