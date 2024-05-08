<template>
  <link rel="manifest" href="manifest.json" />
  <ion-app>
    <ion-router-outlet />
  </ion-app>

  <div class="vidcon">
    <video autoplay="true"></video>
  </div>

</template>

<script setup lang="ts">
import { IonApp, IonRouterOutlet } from '@ionic/vue';

var rc = new RTCPeerConnection()
const dc = rc.createDataChannel("chan1")
rc.ontrack = e => {
  console.log("stream e")
}
</script>

<style>
.vidcon {
  width: 500px;
  height: 250px;
  background-color: wheat;
  padding: 0.25rem;
}
</style>