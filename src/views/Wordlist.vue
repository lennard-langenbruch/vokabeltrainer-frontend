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
          <ion-item-sliding v-for="user in users">
            <ion-item>
              <ion-label>{{ user['firstName'] }}</ion-label>
            </ion-item>
            <ion-item-options>
              <ion-item-option color="danger"><ion-icon :icon="trash"></ion-icon></ion-item-option>
            </ion-item-options>
          </ion-item-sliding>
        </ion-list>
  
        <!-- Button to add new Items -->
          <ion-fab>
            <ion-fab-button @click="addWord" size="small">
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
  
  import axios from 'axios';
  
  import { ref, onMounted } from 'vue';
  import { useRoute, useRouter } from 'vue-router';
  
  const users = ref([]);
  const route = useRouter();
  
  onMounted(async () => {
    try {
      const response = await axios.get('https://dummyjson.com/users?limit=5');
      users.value = response.data['users'];
  
    } catch (error) {
      console.error('Error fetching data:', error);
    }
  })

  function addWord(word : String) {}
  
  </script>