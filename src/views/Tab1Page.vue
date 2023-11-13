<template>
  <ion-page>

    <ion-header>
      <ion-toolbar>
        <ion-title>Hello {username} !</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <ion-card>
        <ion-card-header>
          <ion-card-title><h2>Streak</h2></ion-card-title>
        </ion-card-header>
        <ion-card-content>
          <p>Your current streak is {days} <ion-icon :icon="flame" color="red"></ion-icon></p>
        </ion-card-content>
      </ion-card>

      <ion-card>
        <ion-card-header>
          <ion-card-title><h2>Words of the day</h2></ion-card-title>
        </ion-card-header>
        <ion-card-content>
          <p>Here's a small text description for the card content.</p>
          <p>Nothing more, nothing less.</p>
        </ion-card-content>
      </ion-card>

      <ion-card>
        <ion-card-header>
          <ion-card-title><h2>Tutorial</h2></ion-card-title>
        </ion-card-header>
        <ion-card-content>
          <p>Here you can look up all functionalities of this app !</p>
        </ion-card-content>
      </ion-card>
    </ion-content>

  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle, IonIcon } from '@ionic/vue';
import { flame } from 'ionicons/icons';
//import ExploreContainer from '@/components/ExploreContainer.vue';
</script>
