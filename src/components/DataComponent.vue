<template>
    <div>
      <h1>Usuarios Aleatorios</h1>
      <ul class="data-div">
        <li v-for="user in data" :key="user.uid">
          <div>
            <p><strong>Usuario:</strong> {{ user.first_name }} {{ user.last_name }}</p>
            <p><strong>Correo electrónico:</strong> {{ user.email }}</p>
            <p><strong>Teléfono:</strong> {{ user.phone_number }}</p>
          </div>
        </li>
      </ul>
    </div>
  </template>
  
  
  <script>
  export default {
    data() {
      return {
        data: [],
      };
    },
    mounted() {
      this.fetchData();
    },
    methods: {
      fetchData() {
        fetch('https://random-data-api.com/api/v2/users?size=3')
          .then((response) => response.json())
          .then((data) => {
            this.data = data;
          })
          .catch((error) => {
            console.error('Error al cargar datos:', error);
          });
      },
    },
  };
  </script>
  