<template>
  <q-layout view="lHr lpR fff">

    <q-header bordered class="bg-white text-black">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" />

        <q-toolbar-title class="text-weight-bold">
          Qwitter
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="left" side="left" bordered width="283">
     <q-icon
       class='q-pa-md'
       name='fas fa-dove'
       size='lg'
       color='primary'
       />

<template>
  <div class="q-pa-md" style="max-width: 350px">
    <q-list>
      <q-item to="/" clickable v-ripple>
        <q-item-section avatar>
          <q-icon  name="home" size="md" />
        </q-item-section>

        <q-item-section class="text-h6 text-weight-bold">Home</q-item-section>
      </q-item>

      <q-item to="/about" clickable v-ripple>
        <q-item-section avatar>
          <q-icon name="help" size="md" />
        </q-item-section>

        <q-item-section class="text-h6 text-weight-bold">About</q-item-section>
      </q-item>

    </q-list>

  </div>
</template>
</q-drawer>

    <q-drawer show-if-above v-model="right" side="right" bordered>
       <q-input
        placeholder="Search Qwitter"
        outlined
        rounded
        dense
        v-model="text"
        class="q-ma-md"
       >
        <template v-slot:prepend>
          <q-icon name="search" />
        </template>
      </q-input>

    <q-list bordered padding separator>
      <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-gray">Education</q-item-label>
          <q-item-label>something amazing happened</q-item-label>
          <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>

     <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-gray">Education</q-item-label>
          <q-item-label>something amazing happened</q-item-label>
          <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>

     <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-gray">Education</q-item-label>
          <q-item-label>something amazing happened</q-item-label>
          <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      left: false,
      right: false
    }
  }
}
</script>
