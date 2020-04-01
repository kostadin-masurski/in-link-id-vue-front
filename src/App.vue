<template>
  <div id="app">
    <navigation></navigation>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <home></home>
    <foot></foot>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Home from './components/Home.vue'
import Navigation from './components/core/Navigation.vue'
import Foot from './components/core/Foot.vue'

export default {
  name: 'App',
  components: {
    Navigation,
    HelloWorld,
    Home,
    Foot
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Lato&display=swap");

main div.main-content {
    display: flex;
}

main div.main-content .subject-info {
    padding: 1%;
}

main div.main-content .subject-info p {
    font-size: 18px;
}

main .content-info {
    width: 80%;
    padding: 1%;
    font-size: 18px;
    display: block;
}

main .content-info .user-form input {
    padding: 1%;
    width: 25%;
    border: none;
    border-bottom: 1px solid black;
    font-size: 16px;
    font-family: inherit;
}

main .content-info .user-form input:focus {
    background: rgb(255, 248, 198);
}

main .content-info .user-form .form-group {
    margin-bottom: 1%;
}

main .content-info .user-form .form-group img {
    vertical-align: bottom;
}

main .content-info .user-form button {
    padding: 1%;
    background: #44a9f8;
    color: white;
    border: none;
    width: 10%;
    font-size: 16px;
    cursor: pointer;
}

main .content-info .user-links a {
    color: black;
    text-decoration: none;
    font-weight: normal;
    margin: 2%;
}

main .content-info .user-links a:hover {
    color: #44a9f8;
    text-decoration: underline;
}

main .content-info .user-links .active-route {
    color: #44a9f8;
    text-decoration: underline;
}

/** ************************************** **/

.btn:hover {
    color: #44a9f8;
    background: white;
    border: 1px solid #44a9f8;
    text-decoration: underline;
}

div.form-group {
    margin-top: 1%;
    margin-bottom: 1%;
}

div.form-group input, option, select {
    font-size: 18px;
    padding: 1%;
    width: 25%;
    border: none;
    border-bottom: 1px solid black;
    font-size: 16px;
    font-family: inherit;
    text-align: center;
	text-align-last: center;
}

select {
    -webkit-appearance: none;
    -moz-appearance: none;
    text-indent: 1px;
    text-overflow: '';
}

.content-preview {
    text-align: left;
    word-wrap: break-word;
    display: block;
    width: 100%;
}
</style>
