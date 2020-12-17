<template>
  <div>
    <b-navbar toggleable type="light" variant="light">
      <b-navbar-brand href="#">Mi App</b-navbar-brand>

      <div class="items">
        <b-nav-item>INICIO</b-nav-item>
        <b-nav-item>BUSCAR</b-nav-item>
        <b-nav-item>ACERCA DE</b-nav-item> 
      </div>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">

          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <em>User</em>
            </template>
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    <b-container class="my-5 bv-example-row">
      <b-card-group>
        <b-row>
          <b-col cols="6" sm="8" md="4" lg="4" xl="4" v-for="(pers, index) in pers" :key="index"></b-col>
          <b-card>
            <img :src="pers.imagen" alt="Imagen" img-top>
            <b-card-text>{{pers.nombre}}</b-card-text>
          </b-card>          
        </b-row>
      </b-card-group>      
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'Layout',
  data() {
    return {
      pers: [
        {
          id: 1,
          nombre: 'Morty Smith',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
        },
        {
          id: 2,
          nombre: 'Rick Sánchez',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {
          id: 3,
          nombre: 'Summer Smith',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
        },
        {
          id: 4,
          nombre: 'Beth Smith',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
        },
        {
          id: 5,
          nombre: 'Jerry Smith',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.items {
  list-style: none;
  display: flex;
  justify-content: end;
}
</style>
