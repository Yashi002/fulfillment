<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-back-button slot="start" default-href="/" />
        <ion-title>Upload Csv</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <div class="upload-csv">
        <ion-item>
           <ion-label>Shipped orders</ion-label>
           <ion-input placeholder="Select CSV" />
           <ion-button fill="outline">Upload</ion-button>
        </ion-item>

        <ion-list>
          <ion-list-header>Select the column index for the following information in the uploaded CSV</ion-list-header>
          <ion-item>
            <ion-label>Order ID</ion-label>
            <ion-select placeholder="select">
              <ion-select-option>1234</ion-select-option>
              <ion-select-option>5678</ion-select-option>
              <ion-select-option>9012</ion-select-option>
            </ion-select>
          </ion-item>
           <ion-item>
            <ion-label>Order Shipment ID</ion-label>
            <ion-select placeholder="select">
              <ion-select-option>1234</ion-select-option>
              <ion-select-option>5678</ion-select-option>
              <ion-select-option>9012</ion-select-option>
            </ion-select>
          </ion-item>
           <ion-item>
            <ion-label>Tracking ID</ion-label>
            <ion-select placeholder="select">
              <ion-select-option>1234</ion-select-option>
              <ion-select-option>5678</ion-select-option>
              <ion-select-option>9012</ion-select-option>
            </ion-select>
          </ion-item>
        </ion-list>

        <ion-button expand="block" size="large">Save</ion-button>

        <ion-item>
          <ion-label>50 shipments ready to ship</ion-label>
          <ion-button slot="end" fill="outline">
            <ion-icon slot="start" :icon="downloadOutline" />
            Download  
          </ion-button>
        </ion-item>

      </div>
    </ion-content> 
  </ion-page>
</template>

<script lang="ts">
import { 
  IonBackButton,
  IonButton, 
  IonContent, 
  IonHeader, 
  IonIcon,
  IonInput,
  IonItem, 
  IonLabel, 
  IonList,
  IonListHeader,
  IonPage, 
  IonSelect,
  IonSelectOption,
  IonTitle, 
  IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';
import { downloadOutline } from 'ionicons/icons'

export default defineComponent({
  name: 'UploadCsv',
  components: {
    IonBackButton,
    IonButton, 
    IonContent, 
    IonHeader, 
    IonIcon,
    IonInput,
    IonItem, 
    IonLabel, 
    IonList,
    IonListHeader,
    IonPage, 
    IonSelect,
    IonSelectOption,
    IonTitle, 
    IonToolbar
  },
  setup() {
    return {
      downloadOutline
    }
  }
});
</script>

<style scoped>
.upload-csv {
  max-width: 732px;
  margin: 0 auto;
}
</style>