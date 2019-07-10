# vue-facebook-signin-button-directive

> :closed_lock_with_key: A simple [Vue](https://vuejs.org) directive to include  [Facebook Sign-In Button](https://developers.facebook.com/docs/facebook-login/web?locale=en_US) behavior in any component.

<img src="https://github.com/mejiamanuel57/vue-facebook-signin-button-directive/raw/master/screenshot.jpg" width="677" alt="Screenshot">

## Install

``` bash
$ npm install --save vue-facebook-signin-button-directive

$ yarn add vue-facebook-signin-button-directive
```
## Usage

Import the directive and attach it to any component, let's give you an example:

> Important: `OnFacebookAuthSuccess` and `OnFacebookAuthFail` are mandatory methods you have to declare in your component where you are using the directive.


``` html
<template>
  <button v-facebook-signin-button="appId" class="facebook-signin-button"> Continue with Facebook</button>
</template>

<script>
import FacebookSignInButton from 'vue-facebook-signin-button-directive'
export default {
  directives: {
    FacebookSignInButton
  },
  data: () => ({
    appId: 'Your_Facebook_App-Id'
  }),
  methods: {
    OnFacebookAuthSuccess (idToken) {
      // Receive the idToken and make your magic with the backend
    },
    OnFacebookAuthFail (error) {
      console.log(error)
    }
  }
}
</script>

<style>
.facebook-signin-button {
  color: white;
  background-color: #3b5998;
  height: 50px;
  font-size: 16px;
  border-radius: 10px;
  padding: 10px 20px 25px 20px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>
```


That's all.

[Live example.](https://ramdomizer.com/Account/Login)

> Looking for the [Google counterpart](https://github.com/mejiamanuel57/vue-google-signin-button-directive)?

## License

MIT © [Manuel Mejia Jr.](https://manuelmejiajr.com)
