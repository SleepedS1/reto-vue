<template>
  <ImageComponent/>
  <DataComponent/>
</template>

<script>
import './App.css'
import ImageComponent from './components/ImageComponent.vue';
import DataComponent from './components/DataComponent.vue';

export default {
  name: 'App',
  components: {
    ImageComponent,
    DataComponent
  }
}
</script>

