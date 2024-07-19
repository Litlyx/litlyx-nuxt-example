<script lang="ts" setup>

import { Lit } from 'litlyx-js';

Lit.init("PROJECT_ID");

function onButtonClick() {
  Lit.event('NuxtExampleButtonClick', {
    metadata: {
      title: 'Nuxt is awesome',
      subtitle: 'Litlyx too!'
    }
  })
}

</script>

<template>
  <div class="app">
    <div class="title">
      Litlyx Nuxt Example
    </div>
    <div class="subtitle">
      Follow this steps to start using Litlyx
    </div>
    <div class="text-list">
      <div class="text">
        1. Visit the <a target="_blank" href="https://dashboard.litlyx.com"> Litlyx Dashboard</a> and sign up for an account.
      </div>
      <div class="text">
        2. Once your project is created, copy the `project_id` from the dashboard.
      </div>
      <div class="text">
        3. Replace `PROJECT_ID` in the `Lit.init("PROJECT_ID")` function with your actual `project_id`.
      </div>
      <div class="text">
        4. Reload your Nuxt application to trigger your first visit event.
      </div>
      <div class="text">
        5. (Optional) Click the "Test your event" button to trigger a custom event defined in the `onButtonClick` function.
      </div>
    </div>

    <div class="btn" @click="onButtonClick()"> Test your event </div>

  </div>
</template>


<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

html,
body {
  margin: 0;
  color: white;
}

.btn {
  font-family: "Poppins";
  background-color: rgb(255, 255, 255);
  color: black;
  padding: .2rem 2rem;
  border-radius: .3rem;
  margin-top: 4rem;
  font-weight: 600;
  cursor: pointer;
}

.btn:hover {
  background-color: rgb(221, 221, 221);
}

a {
  font-family: "Poppins";
  color: cyan;
  font-weight: 600;
}

.text-list {
  margin-top: 3rem;
  display: flex;
  flex-direction: column;
  gap: .6rem;
}

.text {
  font-family: "Poppins";
  font-size: 1.1rem;
}

.subtitle {
  font-family: "Poppins";
  font-size: 1.5rem;
}

.title {
  font-size: 3rem;
  font-weight: 600;
  font-family: "Poppins";
  margin-top: 4rem;
}

.app {
  background-color: black;
  width: 100dvw;
  height: 100dvh;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>