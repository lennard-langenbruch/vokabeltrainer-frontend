<template>
  <ion-page>

    <ion-header>
      <ion-toolbar>
        <ion-title>Learning Section &#x1F4A1;</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <!-- Ion List with slideable Ion Items -->
      <ion-list>
        <!-- Item #1 -->
        <ion-item-sliding>
          <ion-item>
            <ion-label>Example Lecture #1</ion-label>
          </ion-item>
          <ion-item-options>
            <ion-item-option ><ion-icon name="trash"></ion-icon></ion-item-option>
          </ion-item-options>
        </ion-item-sliding>
        <!-- Item #2 -->
        <ion-item-sliding>
          <ion-item>
            <ion-label>Example Lecture #2</ion-label>
          </ion-item>
          <ion-item-options>
            <ion-item-option ><ion-icon name="trash"></ion-icon></ion-item-option>
          </ion-item-options>
        </ion-item-sliding>
        <!-- Item #3 -->
        <ion-item-sliding>
          <ion-item>
            <ion-label>Example Lecture #3</ion-label>
          </ion-item>
          <ion-item-options>
            <ion-item-option ><ion-icon name="trash"></ion-icon></ion-item-option>
          </ion-item-options>
        </ion-item-sliding>
      </ion-list>

      <!-- Button to add new Items -->
        <ion-fab>
          <ion-fab-button>
            <ion-icon :icon="add"></ion-icon>
          </ion-fab-button>
        </ion-fab>

    </ion-content>



  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonLabel, IonList,
         IonFab, IonFabButton, IonIcon, IonItemOption, IonItemOptions, IonItemSliding 
} from '@ionic/vue';
import { add, trash } from 'ionicons/icons';
import ExploreContainer from '@/components/ExploreContainer.vue';
</script>
