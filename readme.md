<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, yet powerful, providing tools needed for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of any modern web application framework, making it a breeze to get started learning the framework.

If you're not in the mood to read, [Laracasts](https://laracasts.com) contains over 1100 video tutorials on a range of topics including Laravel, modern PHP, unit testing, JavaScript, and more. Boost the skill level of yourself and your entire team by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for helping fund on-going Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell):

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[British Software Development](https://www.britishsoftware.co)**
- [Fragrantica](https://www.fragrantica.com)
- [SOFTonSOFA](https://softonsofa.com/)
- [User10](https://user10.com)
- [Soumettre.fr](https://soumettre.fr/)
- [CodeBrisk](https://codebrisk.com)
- [1Forge](https://1forge.com)
- [TECPRESSO](https://tecpresso.co.jp/)
- [Pulse Storm](http://www.pulsestorm.net/)
- [Runtime Converter](http://runtimeconverter.com/)
- [WebL'Agence](https://weblagence.com/)

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

## 2. Setup: Installing AdminLTE 3 on Laravel 5.6.7 and Bootstrap 4

1. Install laravel 5.6.7
2. Install the dependencies: npm install
3. Install Admin LTE 3 : npm install admin-lte@v3.0.0-alpha.2 --save
4. Create db and add db credentials to .env
5. Create user (Note: run php artisan migrate:fresh to install new db)
6. Create user : php artisan make:auth
7. Add AdminLTE starter
8. Commit it
9. Modify the starter admin (remove js and css) + /js/app.js; /css/app.css
10. In resources/assets/js/bootstrap.js, add: <require('admin-lte');>
11. In resources/assets/sass/app.js, add: <@import '~admin-lte/dist/css/adminlte.css';>
12. Compile the file: open a new terminal and  npm run watch
13. Git status

	Changes not staged for commit:
	  (use "git add <file>..." to update what will be committed)
	  (use "git checkout -- <file>..." to discard changes in working directory)

	        modified:   public/css/app.css
	        modified:   public/js/app.js
	        modified:   readme.md
	        modified:   resources/assets/js/bootstrap.js
	        modified:   resources/assets/sass/app.scss
	        modified:   resources/views/home.blade.php
	        modified:   resources/views/layouts/master.blade.php

	Untracked files:
	  (use "git add <file>..." to include in what will be committed)

	        public/mix-manifest.json

14. Create repository and push it to Github
15. Test it out :)	        

## 3. Configure Fontawesome 5 with AdminLTE 3 and Laravel 5.6.7

1. Install fontawesome : npm install @fortawesome/fontawesome-free (check package.json file)
2. In resources/assets/sass/app.scss: Add Font Awesome ($fa-font-path: "../webfonts";)
3. In resources/assets/sass/app.scss: import Mixins
	@import '~@fortawesome/fontawesome-free/scss/fontawesome.scss';
	@import '~@fortawesome/fontawesome-free/scss/solid.scss';
	@import '~@fortawesome/fontawesome-free/scss/brands.scss';
4. Modified master.blade.php and added logo, image and icon
5. Git status
	On branch 3_configure_fontawesome                                           
	Changes not staged for commit:                                              
	  (use "git add <file>..." to update what will be committed)                
	  (use "git checkout -- <file>..." to discard changes in working directory) 
	                                                                            
	        modified:   package-lock.json                                       
	        modified:   package.json                                            
	        modified:   public/css/app.css                                      
	        modified:   readme.md                                               
	        modified:   resources/assets/sass/app.scss                          
	        modified:   resources/views/layouts/master.blade.php                
	                                                                            
	Untracked files:                                                            
	  (use "git add <file>..." to include in what will be committed)            
	                                                                            
	        public/fonts/                                                       
	        public/img/                                                         
	                                                                            
	no changes added to commit (use "git add" and/or "git commit -a")           
6. Test it out :)	

## 4. Customizing The AdminLTE 3 

# Left sidebar
1. Display user name
2. Remove active class and change 'Starter Pages' to 'Management' and change the icon with <fas fa-cog>
3. Move Simple Link to under User and change 'Simple Link' to 'Dashboard' and change the icon with this: <fas fa-tachometer-alt> and delete span tag
4. Under Management, create Profile and user icon <fas fa-user>
5. Under Profile, create Logout with icon <fa fa-power-off>	

# Main content
1. Remove all content
2. Git status
	λ git status
	On branch 4_CustomizingTheAdminLTE3
	Changes not staged for commit:
	  (use "git add <file>..." to update what will be committed)
	  (use "git checkout -- <file>..." to discard changes in working directory)

	        modified:   readme.md
	        modified:   resources/views/layouts/master.blade.php

	no changes added to commit (use "git add" and/or "git commit -a")
3. Test it out :)

## 5. Configure Vue Router
1. Got to router.vuejs.org, and install vue-router : npm install vue-router
2. In resources/assets/js/app.js, add this: 
	import VueRouter from 'vue-router';
	Vue.use(VueRouter);
	const routes = [
  		{ path: '/foo', component: require('./components/Dashboard.vue') },
  		{ path: '/bar', component: require('./components/Profile.vue') }
	]
	const router = new VueRouter({
  		routes // short for `routes: routes`
	})

	Put this after last line:
	const app = new Vue({
	    el: '#app',
	    router
	});
3. In resources/assets/js/components, create 2 files: Dashboard.vue and Profile.vue and copy the cotent of ExampleComponent.vue to them 	
4. Add this < <router-view></router-view>> to 'main content' in master
5. Inspect the page and found 2 errors: app.js:14008 CSRF token not found
app.js:36618; and [Vue warn]: Cannot find element: #app
6. Solving the problem: 1. add <id="app"> to div with class wrapper; 2. Add this   <meta name="csrf-token" content="{{ csrf_token() }}"> to master
6. Test it out :)
7. Add link to Dashboar and Profile with <router-link to="/dashboard" class="nav-link"> and <router-link to="profile" class="nav-link">
8. Test the links :)	
9. Git status

λ git status                                                                
On branch 5_configure_vue_router                                            
Changes not staged for commit:                                              
  (use "git add <file>..." to update what will be committed)                
  (use "git checkout -- <file>..." to discard changes in working directory) 
                                                                            
        modified:   package-lock.json                                       
        modified:   package.json                                            
        modified:   public/js/app.js                                        
        modified:   readme.md                                               
        modified:   resources/assets/js/app.js                              
        modified:   resources/views/layouts/master.blade.php                
                                                                            
Untracked files:                                                            
  (use "git add <file>..." to include in what will be committed)            
                                                                            
        resources/assets/js/components/Dashboard.vue                        
        resources/assets/js/components/Profile.vue                          
                                                                            
no changes added to commit (use "git add" and/or "git commit -a")           

## 6. Detect Active Menu in Vue Router and Laravel Plus HTML5 History Mode

1. In app.js, add mode history like this:
	const router = new VueRouter({
	  mode: 'history',	
	  routes // short for `routes: routes`
	})

2. In routes/web.php, add this: 
<Route::get('{path}', "HomeController@index")->where('path', '([A-z\d-\/_.]+)?');>	
3. Remove class 'active' from the master (sidebar)
4. Create active menu: In sass/app.scss add this: 
	<.router-link-exact-active {
		background: #3f51b5;
		color: #fff !important;
	}>
5. Git status
	λ git status
	On branch 6_DetectActiveMenu
	Changes not staged for commit:
	  (use "git add <file>..." to update what will be committed)
	  (use "git checkout -- <file>..." to discard changes in working directory)

	        modified:   public/css/app.css
	        modified:   public/js/app.js
	        modified:   readme.md
	        modified:   resources/assets/js/app.js
	        modified:   resources/assets/sass/app.scss
	        modified:   resources/views/layouts/master.blade.php
	        modified:   routes/web.php

	no changes added to commit (use "git add" and/or "git commit -a")	
5. Test it out :)	