# [Vue Material Dashboard Laravel Pro](https://vue-material-dashboard-laravel-pro.creative-tim.com/?ref=mdpl-readme) [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&logo=twitter)](https://twitter.com/home?status=Vue%20Material%20Dashboard%20Pro%20Laravel%E2%9D%A4%EF%B8%8F%0Ahttps%3A//vue-material-dashboard-laravel-pro.creative-tim.com/%20%23%vue%20%23%material%20%23design%20%23dashboard%20%23laravel%20%23pro%20via%20%40CreativeTim)

![version](https://img.shields.io/badge/version-1.0.1-blue.svg) ![license](https://img.shields.io/badge/license-MIT-blue.svg) [![GitHub issues open](https://img.shields.io/github/issues/creativetimofficial/ct-vue-material-dashboard-laravel-pro.svg?maxAge=2592000)](https://github.com/creativetimofficial/ct-vue-material-dashboard-laravelpro-/issues?q=is%3Aopen+is%3Aissue) [![GitHub issues closed](https://img.shields.io/github/issues-closed-raw/creativetimofficial/ct-vue-material-dashboard-laravel-pro/ct-vue-material-dashboard-laravel-pro.svg?maxAge=2592000)](https://github.com/creativetimofficial/ct-vue-material-dashboard-laravel-pro/issues?q=is%3Aissue+is%3Aclosed)

*Frontend version*: Material Dashboard v2.1.0. More info at https://www.creative-tim.com/product/material-dashboard-pro
*Vue version*: Vue Material Dashboard v1.4.0. More info at https://www.creative-tim.com/product/vue-material-dashboard-pro

![Product Image](https://github.com/creativetimofficial/public-assets/raw/master/vue-material-dashboard-laravel-pro/vue-material-dashboard-laravel-pro.gif?raw=true)

Vue Material Dashboard PRO json API is a fullstack resource built on top of [Vue Material](https://vuematerial.io/) and [Vuejs](https://vuejs.org/v2/guide/). Build awesome-looking apps with a flexible architecture across a variety of devices and operating systems. Vue Material Dashboard PRO json API is the official Vuejs and json API version of the original Material Dashboard PRO.

# Laravel API Setup

## Introduction

JSON:API is a specification for how a client should request that resources be fetched or modified, and how a server should respond to those requests. It is designed to minimize both the number of requests and the amount of data transmitted between clients and servers. This efficiency is achieved without compromising readability, flexibility, or discoverability.

[Click here to go to the JSON:API docs](https://explore.postman.com/api/6357/laravel-jsonapi)

## Prerequisites

The Laravel JSON:API project requires a working Apache/Nginx local environment with PHP, Composer and MySQL.

If you don't already have a local development environment, use one of the following links:

- Windows: [How to install WAMP on Windows](https://updivision.com/blog/post/beginner-s-guide-to-setting-up-your-local-development-environment-on-windows)
- Linux: [How to install LAMP on Linux](https://howtoubuntu.org/how-to-install-lamp-on-ubuntu)
- Mac: [How to install MAMP on MAC](https://wpshout.com/quick-guides/how-to-install-mamp-on-your-mac/)
- Install Composer: [https://getcomposer.org/doc/00-intro.md](https://getcomposer.org/doc/00-intro.md)

## Installation

### via Archive

1. Download the .zip file of the project and extract it:
2. Navigate in your newly cloned project: cd your-json-api-project
3. Install project dependencies: composer install
4. Create a new .env file: cp .env.example .env
5. Generate application key: php artisan key:generate
6. Create users table: php artisan migrate --seed
7. Add your own mailtrap.io credentials in MAIL_USERNAME and MAIL_PASSWORD in the .env file
8. Add your own database credentials in the .env file in DB_DATABASE, DB_USERNAME, DB_PASSWORD
9. Run php artisan passport:client --personal --name="Laravel Personal Access Client"
10. Run php artisan passport:client --password --name="Laravel Password Grant Client"
11. Add the "Laravel Password Grant Client" id to your .env file under the CLIENT_ID key
12. Add the "Laravel Password Grant Client" secret to your .env file under the CLIENT_SECRET key

# Vue Frontend Setup

## Installation
- Install Nodejs from [Nodejs Official Page](https://nodejs.org/en/)
- Open your terminal
- Navigate to the project
- Run `npm install` or `yarn install` if you use [Yarn](https://yarnpkg.com/en/)
- Run `npm run dev` or `yarn serve` to start a local development server
- A new tab will be opened in your browser
- Set your enviroment variables from .env file found in root folder
  - VUE_APP_APP_BASE_URL - The base url of your application
  - VUE_APP_API_BASE_URL - The base url of your API consumed by your application

You can also run additional npm tasks such as
- `npm run build` to build your app for production
- `npm run lint` to run linting.

## Vue-cli

We used the latest 3.x [Vue CLI](https://github.com/vuejs/vue-cli) so you can configure your project in no time. You'll find everything you need inside  `package.json` + some other related files such as `.babelrc`, `.eslintrc.js` and `.postcssrc.js`

## Element-UI

  Vue Material Dashboard PRO json API also uses [element-ui](https://vuematerial.io/ui-elements/elevation) components, restyled to fit perfectly with the existing Material look & feel.

## Usage

To start testing the Pro theme, register as a user or log in using one of the default users: 

- admin type - **admin@material.com** with the password **secret**
- creator type - **creator@material.com** with the password **secret**
- member type - **member@material.com** with the password **secret**

In addition to the features included in the free theme, the Pro theme also has a role management example with an updated user management, as well as tag management, category management and item management examples. All the necessary files are installed out of the box and all the needed routes are added to `src\router\index.js`. Keep in mind that all the features can be viewed once you log in using the credentials provided above or by registering your own user.

Each role has a different privilege level and can perform a certain number of actions according to this level.  

A **member type** user can log in, update his profile and view a list of added items.  
A **creator type** user can log in, update his profile and perform actions on categories, tags and items.
A **admin type** user can log in, update his profile and perform actions on categories, tags, items, roles and users.

### Dashboard

You can access the dashboard either by using the "**Dashboards/Dashboard**" link in the left sidebar or by adding **/home** in the URL.

### Login

The login functionality is fully implemented in our theme helping you to start your project in no time. To login into dashboard you just have to add **/login** in the URL and fill the login form with one of the credentials (user: **admin@material.com**, **creator@material.com**, **member@material.com** and password: **secret**).

The `src\pages\Dashboard\Pages\Login.vue` is the Vue component which handles the login functinality. You can easily adapt it to your needs.

It uses the auth store located in `src\store\modules\auth.js`.

#### Login card
```
<login-card header-color="green">
  <h4 slot="title" class="title">Log in</h4>
  <md-button slot="buttons" ref="#facebook" class="md-just-icon md-simple md-white">
    <i class="fab fa-facebook-square"></i>
  </md-button>
  <md-button slot="buttons" href="#twitter" class="md-just-icon md-simple md-white">
    <i class="fab fa-twitter"></i>
  </md-button>
  <md-button slot="buttons" href="#google" class="md-just-icon md-simple md-white">
    <i class="fab fa-google-plus-g"></i>
  </md-button>
  <p slot="description" class="description">Or Be Classical</p>
  <md-field class="form-group md-invalid" slot="inputs" style="margin-bottom: 28px">
    <md-icon>email</md-icon>
    <label>Email...</label>
    <md-input v-model="email" type="email"/>
    <validation-error :errors="apiValidationErrors.email"/>
  </md-field>
  <md-field class="form-group md-invalid" slot="inputs">
    <md-icon>lock_outline</md-icon>
    <label>Password...</label>
    <md-input v-model="password" type="password"/>
  </md-field>
  <md-button slot="footer" @click="login" class="md-simple md-success md-lg">
    Lets Go
  </md-button>
</login-card>
```
### Register

The register functionality is fully implemented in our theme helping you to start your project in no time. To register a new user you just have to add **/register** in the URL or click on register link from login page and fill the register form with user details.

The `src\pages\Dashboard\Pages\Register.vue` is the Vue component which handles the login functinality. You can easily extend it to your needs.

It uses the auth store located in `src\store\modules\auth.js`.

#### Register card
```
<signup-card>
    <h2 class="title text-center" slot="title">Register</h2>
    <div
        class="md-layout-item md-size-50 md-medium-size-50 md-small-size-100 ml-auto"
        slot="content-left"
    >
        <div
        class="info info-horizontal"
        v-for="item in contentLeft"
        :key="item.title"
        >
        <div :class="`icon ${item.colorIcon}`">
            <md-icon>{{ item.icon }}</md-icon>
        </div>
        <div class="description">
            <h4 class="info-title">{{ item.title }}</h4>
            <p class="description">
            {{ item.description }}
            </p>
        </div>
        </div>
    </div>
    <div
        class="md-layout-item md-size-50 md-medium-size-50 md-small-size-100 mr-auto"
        slot="content-right"
    >
        <div class="social-line text-center">
        <md-button class="md-just-icon md-round md-twitter">
            <i class="fab fa-twitter"></i>
        </md-button>
        <md-button class="md-just-icon md-round md-dribbble">
            <i class="fab fa-dribbble"></i>
        </md-button>
        <md-button class="md-just-icon md-round md-facebook">
            <i class="fab fa-facebook-f"></i>
        </md-button>
        <h4 class="mt-3">or be classical</h4>
        </div>

        <md-field class="md-form-group md-invalid" style="margin-bottom: 2rem">
        <md-icon>face</md-icon>
        <label>Name</label>
        <md-input v-model="name"/>
        <validation-error :errors="apiValidationErrors.name"/>
        </md-field>

        <md-field class="md-form-group md-invalid" style="margin-bottom: 2rem">
        <md-icon>email</md-icon>
        <label>Email</label>
        <md-input v-model="email"/>
        <validation-error :errors="apiValidationErrors.email"/>
        </md-field>

        <md-field class="md-form-group md-invalid" style="margin-bottom: 2rem">
        <md-icon>lock_outline</md-icon>
        <label>Password</label>
        <md-input v-model="password" type="password"/>
        <validation-error :errors="apiValidationErrors.password"/>
        </md-field>

        <md-field class="md-form-group md-invalid">
        <md-icon>lock_outline</md-icon>
        <label>Confirm Password</label>
        <md-input v-model="password_confirmation" type="password"/>
        <validation-error :errors="apiValidationErrors.password_confirmation"/>
        </md-field>

        <md-checkbox v-model="boolean">I agree to the <a>terms and conditions</a>.</md-checkbox>

        <div class="button-container">
        <md-button class="md-success md-round mt-4" @click="register" slot="footer">
            Get Started
        </md-button>
        </div>

    </div>
</signup-card>
```

### Profile edit

You have the option to edit the current logged in user's profile information (name, email, profile picture) and password. To access this page, just click the "**Examples/Profile**" link in the left sidebar or add **/profile** in the URL.

The `src\pages\Dashboard\Examples\UserProfile` is the folder with Vue components that handle the update of the user information and password.

#### Edit profile component
```
<template>
  <form>
    <md-card>

      <md-card-header class="md-card-header-icon">
        <div class="card-icon">
          <md-icon>perm_identity</md-icon>
        </div>
        <h4 class="title">
          Edit Profile
        </h4>
      </md-card-header>

      <md-card-content>
        <div class="md-layout">
          <label class="md-layout-item md-size-15 md-form-label">
            Profile Photo
          </label>
          <div class="md-layout-item">
            <div class="file-input">
              <div v-if="avatar_img">
                <div class="image-container">
                  <img :src="avatar_img"/>
                </div>
              </div>
              <div class="image-container" v-else>
                <img :src="default_img"/>
              </div>
              <div class="button-container">
                <md-button class="md-danger md-round" @click="removeImage" v-if="avatar_img">
                  <i class="fa fa-times"/>
                  Remove
                </md-button>
                <md-button class="md-success md-fileinput">
                  <template v-if="!avatar_img">Select image</template>
                  <template v-else>Change</template>
                  <input type="file" @change="onFileChange"/>
                </md-button>
              </div>
            </div>
          </div>
        </div>

        <div class="md-layout">
          <label class="md-layout-item md-size-15 md-form-label">
            Name
          </label>
          <div class="md-layout-item">
            <md-field class="md-invalid">
              <md-input v-model="user.name"/>
              <validation-error :errors="apiValidationErrors.name"/>
            </md-field>
          </div>
        </div>

        <div class="md-layout">
          <label class="md-layout-item md-size-15 md-form-label">
            Email
          </label>
          <div class="md-layout-item">
            <md-field class="md-invalid">
              <md-input v-model="user.email"/>
              <validation-error :errors="apiValidationErrors.email"/>
            </md-field>
          </div>
        </div>

      </md-card-content>

      <md-card-actions>
        <md-button @click="updateProfile()">
          Update Profile
        </md-button>
      </md-card-actions>

    </md-card>
  </form>
</template>
<script>
  import {ValidationError} from "@/components";
  import formMixin from "@/mixins/form-mixin";

  export default {
    name: "edit-profile-card",

    props: {
      user: Object
    },

    components: {ValidationError},

    mixins: [formMixin],

    data() {
      return {
        avatar_img: null,
        default_img: process.env.VUE_APP_APP_BASE_URL + "/img/placeholder.jpg",
        file: null
      }
    },

    methods: {

      onFileChange(e) {
        let files = e.target.files || e.dataTransfer.files;
        if (!files.length) return;
        this.createImage(files[0]);
      },

      createImage(file) {
        let reader = new FileReader();
        reader.onload = e => {
          this.avatar_img = e.target.result;
          this.file = file;
        }
        reader.readAsDataURL(file);
      },

      removeImage() {
        this.avatar_img = null;
      },

      async updateProfile() {
        try {
          if (!this.user.profile_image) {
            await this.$store.dispatch("users/upload", {user: this.user, image: this.file})
            this.user.profile_image = await this.$store.getters["profile/url"]
          }
          await this.$store.dispatch("profile/update", this.user)
          await this.$store.dispatch("alerts/success", "Profile updated successfully.")
          this.user = await this.$store.getters["profile/me"]
        } catch (e) {
          await this.$store.dispatch("alerts/error", "Oops, something went wrong!")
          this.setApiValidation(e.response.data.errors)
        }

      }

    }
  };
</script>
```

#### Edit password component

```
<template>
  <form ref="password_form">

    <md-card>

      <md-card-header class="md-card-header-icon">
        <div class="card-icon">
          <md-icon>perm_identity</md-icon>
        </div>
        <h4 class="title">
          Change Password
        </h4>
      </md-card-header>

      <md-card-content>
        <div class="md-layout">
          <div class="md-layout-item md-size-100">
            <md-field class="md-invalid">
              <label>Current Password</label>
              <md-input v-model="password" type="password"/>
              <validation-error :errors="apiValidationErrors.password"/>
            </md-field>
            <md-field class="md-invalid">
              <label>New Password</label>
              <md-input v-model="new_password" type="password"/>
              <validation-error :errors="apiValidationErrors.password_confirmation"/>
            </md-field>
            <md-field class="md-invalid">
              <label>Confirm New Password</label>
              <md-input v-model="confirm_password" type="password"/>
              <validation-error :errors="apiValidationErrors.password_confirmation"/>
            </md-field>
          </div>
        </div>
      </md-card-content>

      <md-card-actions>
        <md-button @click="changePassword()">
          Change Password
        </md-button>
      </md-card-actions>
    </md-card>

  </form>
</template>

<script>
  import {ValidationError} from "@/components";
  import formMixin from "@/mixins/form-mixin";
  export default {
    name: "edit-password-card",

    props: {
      user: Object
    },

    components: {ValidationError},

    mixins: [formMixin],

    data: () => ({
      password: null,
      new_password: null,
      confirm_password: null
    }),

    methods: {
      async changePassword() {

        this.user.password = this.password;
        this.user.password_new = this.new_password;
        this.user.password_confirmation = this.confirm_password;

        try {
          await this.$store.dispatch("users/update", this.user)
          await this.$store.dispatch("alerts/error", "Password changed successfully.")
          this.user = await this.$store.getters["profile/me"]
          this.$refs['password_form'].reset()
        } catch (e) {
          await this.$store.dispatch("alerts/error", "Oops, something went wrong!")
          this.setApiValidation(e.response.data.errors)
        }

      }
    }
  };
</script>
```

### Role management

The Pro theme allows you to add user roles. By default, the theme comes with **Admin**, **Creator** and **Member** roles. To access the role management example click the "**Examples/Role Management**" link in the left sidebar or add **/role** to the URL. Here you can add/edit new roles.
To add a new role, click the "**Add role**" button. To edit an existing role, click the dotted menu (available on every table row) and then click "**Edit**". In both cases, you will be directed to a form which allows you to modify the name and description of a role.

The store used for role functionality is found in `src\store\role-module.vue`

You can find the compoments for role functionality in `src\pages\Dashboard\Examples\RoleManagement` folder.

#### List page

```
<md-table
    :value="table"
    :md-sort.sync="sortation.field"
    :md-sort-order.sync="sortation.order"
    :md-sort-fn="customSort"
    class="paginated-table table-striped table-hover"
    >
    <md-table-toolbar>

        <md-field>
        <label>Per page</label>
        <md-select v-model="pagination.perPage" name="pages">
            <md-option
            v-for="item in pagination.perPageOptions"
            :key="item"
            :label="item"
            :value="item"
            >
            {{ item }}
            </md-option>
        </md-select>
        </md-field>

        <md-field>
        <md-input
            v-model="query"
            type="search"
            class="mb-3"
            clearable
            style="width: 200px"
            placeholder="Search ..."
        >
        </md-input>
        </md-field>

    </md-table-toolbar>

    <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Name" md-sort-by="name">{{item.name}}</md-table-cell>
        <md-table-cell md-label="Created At" md-sort-by="created_at">{{item.created_at}}</md-table-cell>
        <md-table-cell md-label="Actions">
        <md-button class="md-icon-button md-raised md-round md-info" @click="goToEdit(item.id)"
                    style="margin: .2rem;">
            <md-icon>edit</md-icon>
        </md-button>
        <md-button class="md-icon-button md-raised md-round md-danger" @click="destroy(item.id)"
                    style="margin: .2rem;">
            <md-icon>delete</md-icon>
        </md-button>
        </md-table-cell>
    </md-table-row>
</md-table>
```

#### Add/edit role
```
<div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Name
    </label>
    <div class="md-layout-item">
        <md-field class="md-invalid">
        <md-input v-model="role.name"/>
        <validation-error :errors="apiValidationErrors.name"/>
        </md-field>
    </div>
</div>
```

### User management

The theme comes with an out of the box user management option. To access this option ,click the "**Examples/User Management**" link in the left sidebar or add **/user** to the URL.
The first thing you will see is a list of existing users. You can add new ones by clicking the "**Add user**" button (above the table on the right). On the Add user page, you will find a form which allows you to fill out the user`s name, email, role and password.

The store used for role functionality is found in `src\store\user-module.vue`

You can find the compoments for role functionality in `src\pages\Dashboard\Examples\UserManagement` folder.

Once you add more users, the list will grow and for every user you will have edit and delete options (access these options by clicking the three dotted menu that appears at the end of every row).

```
<md-table
    :value="table"
    :md-sort.sync="sortation.field"
    :md-sort-order.sync="sortation.order"
    :md-sort-fn="customSort"
    class="paginated-table table-striped table-hover"
    >
    <md-table-toolbar>

        <md-field>
        <label>Per page</label>
        <md-select v-model="pagination.perPage" name="pages">
            <md-option
            v-for="item in pagination.perPageOptions"
            :key="item"
            :label="item"
            :value="item"
            >
            {{ item }}
            </md-option>
        </md-select>
        </md-field>

        <md-field>
        <md-input
            v-model="query"
            type="search"
            class="mb-3"
            clearable
            style="width: 200px"
            placeholder="Search ..."
        >
        </md-input>
        </md-field>

    </md-table-toolbar>

    <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Avatar">
        <md-avatar>
            <img :src="item.profile_image" alt="avatar">
        </md-avatar>
        </md-table-cell>
        <md-table-cell md-label="Name" md-sort-by="name">{{item.name}}</md-table-cell>
        <md-table-cell md-label="Email" md-sort-by="email">{{item.email}}</md-table-cell>
        <md-table-cell md-label="Role" md-sort-by="roles.name">{{item.roles[0].name}}</md-table-cell>
        <md-table-cell md-label="Created At" md-sort-by="created_at">{{item.created_at}}</md-table-cell>
        <md-table-cell md-label="Actions">
        <md-button class="md-icon-button md-raised md-round md-info" @click="goToEdit(item.id)"
                    style="margin: .2rem;">
            <md-icon>edit</md-icon>
        </md-button>
        <md-button class="md-icon-button md-raised md-round md-danger" @click="destroy(item.id)"
                    style="margin: .2rem;">
            <md-icon>delete</md-icon>
        </md-button>
        </md-table-cell>
    </md-table-row>
</md-table>
```

### Tag management

Out of the box you will have an example of tag management (for the cases in which you are developing a blog or a shop). To access this example, click the "**Examples/Tag Management**" link in the left sidebar or add **/tag** to the URL.
You can add and edit tags here, but you can only delete them if they are not attached to any items.

The store used for role functionality is found in `src\store\tag-module.vue`

You can find the compoments for role functionality in `src\pages\Dashboard\Examples\TagManagement` folder.

```
<md-table
    :value="table"
    :md-sort.sync="sortation.field"
    :md-sort-order.sync="sortation.order"
    :md-sort-fn="customSort"
    class="paginated-table table-striped table-hover"
    >
    <md-table-toolbar>

        <md-field>
        <label>Per page</label>
        <md-select v-model="pagination.perPage" name="pages">
            <md-option
            v-for="item in pagination.perPageOptions"
            :key="item"
            :label="item"
            :value="item"
            >
            {{ item }}
            </md-option>
        </md-select>
        </md-field>

        <md-field>
        <md-input
            v-model="query"
            type="search"
            class="mb-3"
            clearable
            style="width: 200px"
            placeholder="Search ..."
        >
        </md-input>
        </md-field>

    </md-table-toolbar>

    <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Name" md-sort-by="name">{{item.name}}</md-table-cell>
        <md-table-cell md-label="Color" md-sort-by="color">
        <span class="badge badge-default" :style="{backgroundColor: item.color}">{{item.name}}</span>
        </md-table-cell>
        <md-table-cell md-label="Created At" md-sort-by="created_at">{{item.created_at}}</md-table-cell>
        <md-table-cell md-label="Actions">
        <md-button class="md-icon-button md-raised md-round md-info" @click="goToEdit(item.id)"
                    style="margin: .2rem;">
            <md-icon>edit</md-icon>
        </md-button>
        <md-button class="md-icon-button md-raised md-round md-danger" @click="destroy(item.id)"
                    style="margin: .2rem;">
            <md-icon>delete</md-icon>
        </md-button>
        </md-table-cell>
    </md-table-row>
</md-table>
```

### Category management 

Out of the box you will have an example of category management (for the cases in which you are developing a blog or a shop). To access this example, click the "**Examples/Category Management**" link in the left sidebar or add **/category** to the URL.
You can add and edit categories here, but you can only delete them if they are not attached to any items.

The store used for category functionality is found in `src\store\categories-module.vue`

You can find the compoments for category functionality in `src\pages\Dashboard\Examples\CategoryManagement` folder.

```
<md-table
    :value="usersTable"
    :md-sort.sync="sortation.field"
    :md-sort-order.sync="sortation.order"
    :md-sort-fn="customSort"
    class="paginated-table table-striped table-hover"
    >
    <md-table-toolbar>

        <md-field>
        <label>Per page</label>
        <md-select v-model="pagination.perPage" name="pages">
            <md-option
            v-for="item in pagination.perPageOptions"
            :key="item"
            :label="item"
            :value="item"
            >
            {{ item }}
            </md-option>
        </md-select>
        </md-field>

        <md-field>
        <md-input
            v-model="query"
            type="search"
            class="mb-3"
            clearable
            style="width: 200px"
            placeholder="Search ..."
        >
        </md-input>
        </md-field>

    </md-table-toolbar>

    <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Name" md-sort-by="name">{{item.name}}</md-table-cell>
        <md-table-cell md-label="Description" md-sort-by="description">{{item.description}}</md-table-cell>
        <md-table-cell md-label="Created At" md-sort-by="created_at">{{item.created_at}}</md-table-cell>
        <md-table-cell md-label="Actions">
        <md-button class="md-icon-button md-raised md-round md-info" @click="goToEdit(item.id)"
                    style="margin: .2rem;">
            <md-icon>edit</md-icon>
        </md-button>
        <md-button class="md-icon-button md-raised md-round md-danger" @click="destroy(item.id)"
                    style="margin: .2rem;">
            <md-icon>delete</md-icon>
        </md-button>
        </md-table-cell>
    </md-table-row>
</md-table>

```

### Item management

Item management is the most advanced example included in the Pro theme, because every item has a picture, belongs to a category and has multiple tags. To access this example click the "**Examples/Item Management**" link in the left sidebar or add **/item** to the URL.
Here you can manage the items. A list of items will appear once you start adding them (to access the add page click "**Add item**").
On the add page, besides the Name and Description fields (which are present in most of the CRUD examples) you can see a category dropdown, which contains the categories you added, a file input and a tag multi select. If you did not add any categories or tags, please go to the corresponding sections (category management, tag management) and add some.  

The store used for roles functionality is found in `src\store\items-module.vue`

You can find the compoments for items functionality in `src\pages\Dashboard\Examples\ItemManagement` folder.

#### List Items
```
<md-table
    :value="table"
    :md-sort.sync="sortation.field"
    :md-sort-order.sync="sortation.order"
    :md-sort-fn="customSort"
    class="paginated-table table-striped table-hover"
    >
    <md-table-toolbar>

        <md-field>
        <label>Per page</label>
        <md-select v-model="pagination.perPage" name="pages">
            <md-option
            v-for="item in pagination.perPageOptions"
            :key="item"
            :label="item"
            :value="item"
            >
            {{ item }}
            </md-option>
        </md-select>
        </md-field>

        <md-field>
        <md-input
            v-model="query"
            type="search"
            class="mb-3"
            clearable
            style="width: 200px"
            placeholder="Search ..."
        >
        </md-input>
        </md-field>

    </md-table-toolbar>

    <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Name" md-sort-by="name">{{item.name}}</md-table-cell>
        <md-table-cell md-label="Category" md-sort-by="category.name">{{item.category.name}}</md-table-cell>
        <md-table-cell md-label="Picture">
            <md-avatar>
            <img :src="item.image" alt="avatar">
            </md-avatar>
        </md-table-cell>
        <md-table-cell md-label="Tags" md-sort-by="tags.name">
        <span v-for="(tag, index) in item.tags" :key="'tag' + index" class="badge badge-default" :style="{backgroundColor: tag.color, margin: '.1rem'}">
            {{tag.name}}
        </span>
        </md-table-cell>
        <md-table-cell md-label="Created At" md-sort-by="created_at">{{item.created_at}}</md-table-cell>
        <md-table-cell md-label="Actions">
        <md-button class="md-icon-button md-raised md-round md-info" @click="goToEdit(item.id)" style="margin: .2rem;">
            <md-icon>edit</md-icon>
        </md-button>
        <md-button class="md-icon-button md-raised md-round md-danger" @click="destroy(item.id)" style="margin: .2rem;">
            <md-icon>delete</md-icon>
        </md-button>
        </md-table-cell>
    </md-table-row>
</md-table>
```

#### Add/Edit Item
```
<md-card-content>

    <div class="text-right">
    <md-button @click="goBack" class="md-primary md-dense">
        Back to List
    </md-button>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Profile Photo
    </label>
    <div class="md-layout-item">
        <div class="file-input">
        <div v-if="image">
            <div class="image-container">
            <img :src="image"/>
            </div>
        </div>
        <div class="image-container" v-else>
            <img :src="default_image"/>
        </div>
        <div class="button-container">
            <md-button class="md-danger md-round" @click="removeImage" v-if="image">
            <i class="fa fa-times"/>
            Remove
            </md-button>
            <md-button class="md-success md-fileinput">
            <template v-if="!image">Select image</template>
            <template v-else>Change</template>
            <input type="file" @change="onFileChange"/>
            </md-button>
        </div>
        </div>
    </div>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Name
    </label>
    <div class="md-layout-item">
        <md-field class="md-invalid">
        <md-input v-model="item.name"/>
        <validation-error :errors="apiValidationErrors.name"/>
        </md-field>
    </div>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Description
    </label>
    <div class="md-layout-item">
        <md-field class="md-invalid">
        <md-textarea v-model="item.description"/>
        <validation-error :errors="apiValidationErrors.excerpt"/>
        </md-field>
    </div>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Category
    </label>
    <div class="md-layout-item">
        <md-field>
        <label>Select ...</label>
        <md-select v-model="item.category.id" name="categories">
            <md-option v-for="category in available_categories"
                        :key="category.id"
                        :value="category.id"
            >
            {{ category.name }}
            </md-option>
        </md-select>
        </md-field>
    </div>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Tags
    </label>
    <div class="md-layout-item">
        <md-field>
        <label>Select ...</label>
        <md-select v-model="tags" @md-selected="updateTags" name="tags" multiple>
            <md-option v-for="tag in available_tags"
                        :key="'tag_' + tag.id"
                        :value="tag.id"
            >
            {{ tag.name }}
            </md-option>
        </md-select>
        </md-field>
    </div>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Status
    </label>
    <div class="md-layout-item">
        <md-field>
        <md-radio v-model="item.status" value="published">Published</md-radio>
        <md-radio v-model="item.status" value="draft">Draft</md-radio>
        <md-radio v-model="item.status" value="archive">Archive</md-radio>
        </md-field>
    </div>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Show on homepage?
    </label>
    <div class="md-layout-item">
        <md-field>
        <md-switch v-model="item.is_on_homepage"/>
        </md-field>
    </div>
    </div>

    <div class="md-layout">
    <label class="md-layout-item md-size-25 md-form-label">
        Date
    </label>
    <div class="md-layout-item">
        <md-datepicker v-model="date_at" :class="{'md-invalid': !!apiValidationErrors.date_at}">
        <label>Select date ...</label>
        <validation-error :errors="apiValidationErrors.date_at"/>
        </md-datepicker>
    </div>
    </div>

</md-card-content>
```

## Table of Contents

* [Versions](#versions)
* [Demo](#demo)
* [Documentation](#documentation)
* [File Structure](#file-structure)
* [Browser Support](#browser-support)
* [Resources](#resources)
* [Reporting Issues](#reporting-issues)
* [Licensing](#licensing)
* [Useful Links](#useful-links)

## Versions

[<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/512px-HTML5_logo_and_wordmark.svg.png" height="50" />](#)
[<img src="https://logos-download.com/wp-content/uploads/2016/09/Laravel_logo-700x508.png" height="50" />](#)
[<img src="https://s3.amazonaws.com/creativetim_bucket/github/vuejs.png" height="50" style="vertical-align: super" />](#)
[<img src="https://jsonapi.org/images/jsonapi.png" height="60" style="vertical-align: super" />](#)


| HTML | LARAVEL | VUE | LARAVEL & VUE|
| --- | --- | --- | --- |
| [![Material Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/51/thumb/opt_mdp_thumbnail.jpg?1521134752)](https://demos.creative-tim.com/material-dashboard-pro/examples/dashboard.html?ref=vmdpl-readme) | [![Material Dashboard Pro Laravel](https://s3.amazonaws.com/creativetim_bucket/products/158/thumb/opt_mdp_laravel_thumbnail.jpg)](https://material-dashboard-pro-laravel.creative-tim.com/?ref=vmdpl-readme) | [![Vue Material Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/87/thumb/opt_mdp_vue_thumbnail.jpg)](https://www.creative-tim.com/product/vue-material-dashboard-pro?ref=vmdpl-readme) | [![Vue Material Dashboard Laravel Pro](https://s3.amazonaws.com/creativetim_bucket/products/87/thumb/opt_mdp_vue_thumbnail.jpg)](https://www.creative-tim.com/product/vue-material-dashboard-pro?ref=vmdpl-readme) |

## Demo

| Register | Login | Dashboard |
| --- | --- | ---  |
| [![Register](https://github.com/creativetimofficial/public-assets/raw/master/vue-material-dashboard-laravel-pro/Register.png)](https://material-dashboard-pro-laravel.creative-tim.com/register?ref=vmdpl-readme)  | [![Login](https://github.com/creativetimofficial/public-assets/raw/master/vue-material-dashboard-laravel-pro/Login.png)](https://material-dashboard-pro-laravel.creative-tim.com/login?ref=vmdpl-readme)  | [![Dashboard](https://github.com/creativetimofficial/public-assets/raw/master/vue-material-dashboard-laravel-pro/Dashboard.png)](https://material-dashboard-pro-laravel.creative-tim.com/?ref=vmdpl-readme) |

| Profile Page | Users Page | Tables Page  |
| --- | --- | ---  |
| [![Profile Page](https://github.com/creativetimofficial/public-assets/raw/master/vue-material-dashboard-laravel-pro/Profile.png)](https://vue-material-dashboard-laravel-pro.creative-tim.com/profile?ref=vmdpl-readme)  | [![Users Page](https://github.com/creativetimofficial/public-assets/raw/master/vue-material-dashboard-laravel-pro/Users.png)](https://vue-material-dashboard-laravel-pro.creative-tim.com/user?ref=vmdpl-readme) | [![Tables Page](https://github.com/creativetimofficial/public-assets/raw/master/vue-material-dashboard-laravel-pro/Tables.png)](https://vue-material-dashboard-laravel-pro.creative-tim.com/table-list?ref=vmdpl-readme)
[View More](https://vue-material-dashboard-laravel-pro.creative-tim.com/?ref=vmdpl-readme)

## Documentation
The documentation for the Vue Material Dashboard Laravel Pro is hosted at our [website](https://vue-material-dashboard-laravel-pro.creative-tim.com/documentation?ref=vmdpl-readme).

## File Structure
```
|   .browserslistrc
|   .env
|   .eslintrc.js
|   .gitignore
|   .jshintrc
|   babel.config.js
|   CHANGELOG.md
|   package.json
|   postcss.config.js
|   README.md
|   yarn.lock
|
+---public
|   |   .DS_Store
|   |   favicon.png
|   |   index.html
|   |
|   \---img
|       |   apple-icon.png
|       |   bg-pricing.jpg
|       |   bg3.jpg
|       |   bg9.jpg
|       |   card-1.jpg
|       |   card-2.jpg
|       |   card-3.jpg
|       |   default-avatar.png
|       |   favicon.png
|       |   image_placeholder.jpg
|       |   lock.jpg
|       |   login.jpg
|       |   mask.png
|       |   new_logo.png
|       |   placeholder.jpg
|       |   product1.jpg
|       |   product2.jpg
|       |   product3.jpg
|       |   register.jpg
|       |   sidebar-1.jpg
|       |   sidebar-2.jpg
|       |   sidebar-3.jpg
|       |   sidebar-4.jpg
|       |   vue-logo.png
|       |
|       +---faces
|       |       avatar.jpg
|       |       card-profile1-square.jpg
|       |       card-profile2-square.jpg
|       |       marc.jpg
|       |
|       \---flags
|               AU.png
|               BR.png
|               DE.png
|               GB.png
|               RO.png
|               US.png
|
\---src
    |   .DS_Store
    |   App.vue
    |   globalComponents.js
    |   globalDirectives.js
    |   main.js
    |   material-dashboard.js
    |
    +---assets
    |   |   .DS_Store
    |   |
    |   +---css
    |   |       demo.css
    |   |
    |   \---scss
    |       |   .DS_Store
    |       |   material-dashboard.scss
    |       |
    |       \---md
    |           |   .DS_Store
    |           |   _alerts.scss
    |           |   _autocomplete.scss
    |           |   _badges.scss
    |           |   _buttons.scss
    |           |   _cards.scss
    |           |   _chartist.scss
    |           |   _checkboxes.scss
    |           |   _collapse.scss
    |           |   _colors.scss
    |           |   _dialogs.scss
    |           |   _dropdown.scss
    |           |   _fileinput.scss
    |           |   _fixed-plugin.scss
    |           |   _footers.scss
    |           |   _forms.scss
    |           |   _headers.scss
    |           |   _info-areas.scss
    |           |   _inputs-size.scss
    |           |   _inputs.scss
    |           |   _layout.scss
    |           |   _misc.scss
    |           |   _mixins.scss
    |           |   _navbars.scss
    |           |   _pages.scss
    |           |   _pagination.scss
    |           |   _pills.scss
    |           |   _popups.scss
    |           |   _progress.scss
    |           |   _radios.scss
    |           |   _responsive.scss
    |           |   _rtl.scss
    |           |   _select.scss
    |           |   _shadows.scss
    |           |   _sidebar-and-main-panel.scss
    |           |   _tables.scss
    |           |   _tabs.scss
    |           |   _tags.scss
    |           |   _timeline.scss
    |           |   _togglebutton.scss
    |           |   _typography.scss
    |           |   _variables.scss
    |           |
    |           +---cards
    |           |       _card-global-sales.scss
    |           |       _card-login.scss
    |           |       _card-pricing.scss
    |           |       _card-product.scss
    |           |       _card-profile.scss
    |           |       _card-signup.scss
    |           |       _card-tabs.scss
    |           |       _card-testimonials.scss
    |           |
    |           +---mixins
    |           |       _chartist.scss
    |           |       _sidebar.scss
    |           |       _transparency.scss
    |           |       _vendor-prefixes.scss
    |           |
    |           \---plugins
    |                   _animate.scss
    |                   _fullcalendar.scss
    |                   _md-datepicker.scss
    |                   _perfect-scrollbar.scss
    |                   _plugin-jquery.jvectormap.scss
    |                   _plugin-nouislider.scss
    |                   _sweetalert2.scss
    |                   _wizard-card.scss
    |
    +---components
    |   |   .DS_Store
    |   |   AnimatedNumber.vue
    |   |   Badge.vue
    |   |   Collapse.vue
    |   |   Dropdown.vue
    |   |   index.js
    |   |   Logout.vue
    |   |   Modal.vue
    |   |   Pagination.vue
    |   |   Slider.vue
    |   |   Tabs.vue
    |   |
    |   +---Cards
    |   |       ChartCard.vue
    |   |       GlobalSalesCard.vue
    |   |       LockCard.vue
    |   |       LoginCard.vue
    |   |       NavTabsCard.vue
    |   |       PricingCard.vue
    |   |       ProductCard.vue
    |   |       SignupCard.vue
    |   |       StatsCard.vue
    |   |       TestimonialCard.vue
    |   |
    |   +---Inputs
    |   |       IconCheckbox.vue
    |   |
    |   +---NotificationPlugin
    |   |       index.js
    |   |       Notification.vue
    |   |       Notifications.vue
    |   |
    |   +---SidebarPlugin
    |   |       index.js
    |   |       SideBar.vue
    |   |       SidebarItem.vue
    |   |
    |   +---Tables
    |   |       GlobalSalesTable.vue
    |   |
    |   +---Timeline
    |   |       TimeLine.vue
    |   |       TimeLineItem.vue
    |   |
    |   +---Wizard
    |   |       throttle.js
    |   |       Wizard.vue
    |   |       WizardTab.vue
    |   |
    |   \---WorldMap
    |           AsyncWorldMap.vue
    |           WorldMap.vue
    |           world_map.js
    |
    +---middleware
    |       auth.js
    |       guest.js
    |
    +---pages
    |   |   .DS_Store
    |   |   FixedPlugin.vue
    |   |   index.js
    |   |
    |   \---Dashboard
    |       |   .DS_Store
    |       |   Calendar.vue
    |       |   Charts.vue
    |       |   Dashboard.vue
    |       |   Widgets.vue
    |       |
    |       +---Components
    |       |       Buttons.vue
    |       |       GridSystem.vue
    |       |       Icons.vue
    |       |       Notifications.vue
    |       |       Panels.vue
    |       |       SweetAlert.vue
    |       |       Typography.vue
    |       |
    |       +---Forms
    |       |   |   ExtendedForms.vue
    |       |   |   RegularForms.vue
    |       |   |   ValidationForms.vue
    |       |   |   Wizard.vue
    |       |   |
    |       |   +---ValidationForms
    |       |   |       LoginForm.vue
    |       |   |       RangeValidationForm.vue
    |       |   |       RegisterForm.vue
    |       |   |       TypeValidationForm.vue
    |       |   |
    |       |   \---Wizard
    |       |           FirstStep.vue
    |       |           SecondStep.vue
    |       |           ThirdStep.vue
    |       |
    |       +---Layout
    |       |   |   Content.vue
    |       |   |   ContentFooter.vue
    |       |   |   DashboardLayout.vue
    |       |   |   TopNavbar.vue
    |       |   |
    |       |   \---Extra
    |       |           MobileMenu.vue
    |       |           UserMenu.vue
    |       |
    |       +---Maps
    |       |       API_KEY.js
    |       |       FullScreenMap.vue
    |       |       GoogleMaps.vue
    |       |       VectorMaps.vue
    |       |       WorldMap.vue
    |       |       world_map.js
    |       |
    |       +---Pages
    |       |   |   AuthLayout.vue
    |       |   |   Lock.vue
    |       |   |   Login.vue
    |       |   |   Pricing.vue
    |       |   |   Register.vue
    |       |   |   RtlSupport.vue
    |       |   |   TimeLinePage.vue
    |       |   |   UserProfile.vue
    |       |   |
    |       |   \---UserProfile
    |       |           EditProfileForm.vue
    |       |           UserCard.vue
    |       |
    |       \---Tables
    |               ExtendedTables.vue
    |               PaginatedTables.vue
    |               RegularTables.vue
    |               users.js
    |
    +---routes
    |       router.js
    |       routes.js
    |
    \---store
        |   index.js
        |
        \---modules
                auth.js
```

## Browser Support

At present, we officially aim to support the last two versions of the following browsers:

<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/chrome-logo.png?raw=true" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/firefox-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/edge-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/safari-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/opera-logo.png" width="64" height="64">


## Resources
- Demo: <https://vue-material-dashboard-laravel-pro.creative-tim.com/?ref=vmdpl-readme>
- Download Page: <https://www.creative-tim.com/product/vue-material-dashboard-laravel-pro?ref=vmdpl-readme>
- Documentation: <https://vue-material-dashboard-laravel-pro.creative-tim.com/documentation?ref=vmdpl-readme>
- License Agreement: <https://www.creative-tim.com/license>
- Support: <https://www.creative-tim.com/contact-us>
- Issues: [Github Issues Page](https://github.com/creativetimofficial/ct-vue-material-dashboard-laravel-pro/issues)
- **Dashboards:**

| HTML | LARAVEL | VUE | LARAVEL & VUE|
| --- | --- | --- | --- |
| [![Material Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/51/thumb/opt_mdp_thumbnail.jpg?1521134752)](https://demos.creative-tim.com/material-dashboard-pro/examples/dashboard.html?ref=vmdpl-readme) | [![Material Dashboard Pro Laravel](https://s3.amazonaws.com/creativetim_bucket/products/158/thumb/opt_mdp_laravel_thumbnail.jpg)](https://material-dashboard-pro-laravel.creative-tim.com/?ref=vmdpl-readme) | [![Vue Material Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/87/thumb/opt_mdp_vue_thumbnail.jpg)](https://www.creative-tim.com/product/vue-material-dashboard-pro?ref=vmdpl-readme) | [![Vue Material Dashboard Laravel Pro](https://s3.amazonaws.com/creativetim_bucket/products/87/thumb/opt_mdp_vue_thumbnail.jpg)](https://www.creative-tim.com/product/vue-material-dashboard-pro?ref=vmdpl-readme) |

## Change log

Please see the [changelog](CHANGELOG.md) for more information on what has changed recently.

## Credits

- [Creative Tim](https://creative-tim.com/?ref=vmdpl-readme)
- [UPDIVISION](https://updivision.com)

## Reporting Issues

We use GitHub Issues as the official bug tracker for the Vue Material Dashboard Laravel. Here are some advices for our users that want to report an issue:

1. Make sure that you are using the latest version of the Vue Material Dashboard Laravel. Check the CHANGELOG from your dashboard on our [website](https://www.creative-tim.com/?ref=vmdpl-readme).
2. Providing us reproducible steps for the issue will shorten the time it takes for it to be fixed.
3. Some issues may be browser specific, so specifying in what browser you encountered the issue might help.

## Licensing

- Copyright 2019 Creative Tim (https://www.creative-tim.com/?ref=vmdpl-readme)
- [Creative Tim License](https://www.creative-tim.com/license).


## Useful Links

- [Tutorials](https://www.youtube.com/channel/UCVyTG4sCw-rOvB9oHkzZD1w)
- [Affiliate Program](https://www.creative-tim.com/affiliates/new) (earn money)
- [Blog Creative Tim](http://blog.creative-tim.com/)
- [Free Products](https://www.creative-tim.com/bootstrap-themes/free) from Creative Tim
- [Premium Products](https://www.creative-tim.com/bootstrap-themes/premium?ref=vmdpl-readme) from Creative Tim
- [React Products](https://www.creative-tim.com/bootstrap-themes/react-themes?ref=vmdpl-readme) from Creative Tim
- [Angular Products](https://www.creative-tim.com/bootstrap-themes/angular-themes?ref=vmdpl-readme) from Creative Tim
- [VueJS Products](https://www.creative-tim.com/bootstrap-themes/vuejs-themes?ref=vmdpl-readme) from Creative Tim
- [More products](https://www.creative-tim.com/bootstrap-themes?ref=vmdpl-readme) from Creative Tim
- Check our Bundles [here](https://www.creative-tim.com/bundles??ref=vmdpl-readme)

## Social Media

### Creative Tim:

Twitter: <https://twitter.com/CreativeTim?ref=vmdpl-readme>

Facebook: <https://www.facebook.com/CreativeTim?ref=vmdpl-readme>

Dribbble: <https://dribbble.com/creativetim?ref=vmdpl-readme>

Instagram: <https://www.instagram.com/CreativeTimOfficial?ref=vmdpl-readme>


### Updivision:

Twitter: <https://twitter.com/updivision?ref=vmdpl-readme>

Facebook: <https://www.facebook.com/updivision?ref=vmdpl-readme>

Linkedin: <https://www.linkedin.com/company/updivision?ref=vmdpl-readme>

Updivision Blog: <https://updivision.com/blog/?ref=vmdpl-readme>

## Credits

- [Creative Tim](https://creative-tim.com/?ref=mdpl-readme)
- [UPDIVISION](https://updivision.com)
