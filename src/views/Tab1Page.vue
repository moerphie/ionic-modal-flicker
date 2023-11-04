<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>

      <ExploreContainer name="Tab 1 page" />


      <ion-button id="open-modal" expand="block">Open modal</ion-button>
      <ion-modal ref="modal" id="testModal" trigger="open-modal" :initial-breakpoint="1" :breakpoints="[0, 1]" handle="false">
        <div class="wrapper">
          <h1>Title</h1>
          ...
        </div>
      </ion-modal>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonModal, IonButton } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
import { ref } from 'vue'

const modal = ref()
</script>


<style lang="scss" scoped>
#testModal {
  --height: auto;

  .wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 25rem;
    min-height: 300px;
    margin: 0 auto;

    h1 {
      margin: 0.5rem auto;
    }
  }
}
</style>
