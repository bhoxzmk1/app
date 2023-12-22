<!-- <template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>SOMETHING</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>

      <div id="container">
        <strong>Ready to create an app?</strong>
        <p>Start with Ionic <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">UI Components</a></p>
      </div>
    </ion-content>
  </ion-page>
</template>



<script setup lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
</script> -->









<template>
    <ion-menu content-id="main-content">
      <ion-header>
        <ion-toolbar>
          <ion-title>Chandler Bing</ion-title>
        </ion-toolbar>
  
          <ion-list lines="none">
            <ion-item href="/HomePage.vue">
              <ion-label>Home</ion-label>
            </ion-item>
          </ion-list>
  
          <ion-list lines="none">
            <ion-item href="/order.vue">
              <ion-label>Order</ion-label>
            </ion-item>
          </ion-list>
  
          <ion-list lines="none">
            <ion-item href="/notification.vue">
              <ion-label>Notification</ion-label>
            </ion-item>
          </ion-list>
  
      </ion-header>
      
     
          <ion-toolbar>
            <ion-buttons slot="start">
              <ion-menu-button shape="round" >LOGOUT</ion-menu-button>
            </ion-buttons>
          </ion-toolbar>
  
    </ion-menu>
  
  
  
    <ion-page id="main-content">
      <ion-header>
        <ion-toolbar>
          <ion-buttons slot="start">
            <ion-menu-button></ion-menu-button>
          </ion-buttons>
          <ion-title>Menu</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content class="ion-padding"> NAVIGATION </ion-content>
    </ion-page>
  </template>
  
  
  
  
  
  
  
  <script lang="ts">
    import { 
      IonButtons, 
      IonContent, 
      IonHeader, 
      IonLabel, 
      IonList, 
      IonMenu, 
      IonMenuButton, 
      IonPage, 
      IonTitle, 
      IonToolbar 
    } from '@ionic/vue';
    import { defineComponent } from 'vue';
  
    export default defineComponent({
      components: {
      IonButtons,
      IonContent,
      IonHeader,
      IonMenu,
      IonMenuButton,
      IonPage,
      IonTitle,
      IonToolbar,
      IonList,
      IonLabel
  },
    });
  
    class PageThree extends HTMLElement {
      connectedCallback() {
        this.innerHTML = `
      <ion-header>
        <ion-toolbar>
          <ion-title>Page One</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content class="ion-padding">
        This is the content for page 1.
        <ion-router-link href="#/page-two">
          <ion-button>Go to Page 2</ion-button>
        </ion-router-link>
      </ion-content>`;
      }
    }
  
    class PageFour extends HTMLElement {
      connectedCallback() {
        this.innerHTML = `
      <ion-header>
        <ion-toolbar>
          <ion-buttons slot="start">
            <ion-back-button default-href="/"></ion-back-button>
          </ion-buttons>
          <ion-title>Page Two</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content class="ion-padding">
        This is the content for page 2.
      </ion-content>`;
      }
    }
  
    customElements.define('page-three', PageThree);
    customElements.define('page-four', PageFour);
  
  
  
    // import { IonButton } from '@ionic/vue';
    // import { defineComponent } from 'vue';
  
    // export default defineComponent({
    //   components: { IonButton },
    // });
  
  
  
  </script>
  
  
  
  
  
  
  
  
  
  <style scoped>
  #container {
    text-align: center;
    
    position: absolute;
    left: 0;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
  }
  
  #container strong {
    font-size: 20px;
    line-height: 26px;
  }
  
  #container p {
    font-size: 16px;
    line-height: 22px;
    
    color: #696565;
    
    margin: 0;
  }
  
  #container a {
    text-decoration: none;
  }
  </style>
  