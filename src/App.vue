<template>
  <v-app>

<!--Header-->

  <v-app-bar app color="primary">

    <v-img color="red" max-height="1000" max-width="50" src="logo.png">
  </v-img>
  <v-row
    justify="space-around"
  >
  <v-btn elevation="3" color="white" ><v-icon>mdi-home</v-icon>home</v-btn>

<!--Categorias de Productos-->

  <v-menu transition="slide-y-transition">
      <template v-slot:activator="{ on, attrs }">
  <v-btn elevation="3" color="white" v-bind="attrs" v-on="on"><v-icon>mdi-cart</v-icon>Productos</v-btn>
</template>
<v-list>
        <v-list-item>
          <v-list-item-title><v-img src="conjunto1.png" height="250" width="250"></v-img>Conjuntos</v-list-item-title>
          <v-list-item-title><v-img src="https://assets.adidas.com/images/w_766,h_766,f_auto,q_auto,fl_lossy,c_fill,g_auto/43b50cfb546a4be4ad6aaf6900fac5f9_9366/remera-archive-cut-line.jpg" height="250" width="250"></v-img>Mujeres</v-list-item-title>
          <v-list-item-title><v-img src="pantalon3.png" height="250" width="250"></v-img>Hombres</v-list-item-title>
        </v-list-item>
      </v-list>
  </v-menu>

  <v-btn elevation="3" color="white"><v-icon>mdi-map</v-icon>Nosotros</v-btn>
  <v-btn elevation="3" color="white"><v-icon>mdi-account-circle</v-icon>Contacto</v-btn>
  </v-row>
  </v-app-bar>

<!--Banner-->

<v-main mx="auto">

<v-container>
  <v-row justify="center" >
  <v-card class="mt-15" max-width="1500" :elecation="24" >
    <v-img src="banner.png">
    <v-card-title>50% OFF</v-card-title>
  </v-img>
  <v-card-text>
    <div>Conjunto UniSex</div>
    <div>Negro deportivo</div>
  </v-card-text>

  </v-card>
</v-row>
</v-container>

<!--Carrusel de Imagenes-->

 <v-container>
 <v-row justify="center">
  <v-col   xs="12" sm="6">
    <v-card>
  <v-carousel  hide-delimiter-background >
    <v-carousel-item
      v-for="(imagen,i) in imagenes"
      :key="i"
      :src="imagen.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</v-card>
</v-col>
</v-row>
</v-container>

<!--Productos nuevos-->





<v-container>
  <v-row>
    <v-col cols="4">
      <v-img src="conjunto1.png"></v-img>
    </v-col>
    <v-col cols="4">
      <v-img src="remera2.png"></v-img>
    </v-col>
    <v-col cols="4">
      <v-img src="pantalon3.png"></v-img>
    </v-col>
  </v-row>
</v-container>

</v-main>
<!--Comentarios-->

<v-card>
  <v-card-title>
    
  </v-card-title>
  <v-rating
  empty-icon="$mdi-Star-Out-line"
  full-icon="$mdi-Star"
  half-icon="$mdi-Star-Half-Full"
  hover
  length="5"
  size="64"
  value="3"
></v-rating>
</v-card>
<!--Footer-->

<v-footer color="gray" height="110" class="mt-9" >
  <v-row
    justify="space-around">

<v-col cols="4">Dirección: Pepe Argento 1905</v-col>
<v-col cols="4">Email: EduRopa@gmail.com</v-col>
<v-col cols="4">Telefono: (011) 25074533</v-col>
</v-row>
<v-row justify="space-around" class="mb-4">

<v-btn elevation="4" color="white"><v-icon>mdi-facebook</v-icon></v-btn>
<v-btn elevation="4" color="white"><v-icon>mdi-twitter</v-icon></v-btn>
<v-btn elevation="4" color="white"><v-icon>mdi-instagram</v-icon></v-btn>

  </v-row>
</v-footer>
</v-app>

</template>

<script>
export default {
  data () {
    return {
      imagenes: [
        {
          src: 'https://assets.adidas.com/images/w_276,h_276,f_auto,q_auto,fl_lossy,c_fill,g_auto/ded2b74d43e947138119ae8b01691fa2_9366/GZ4097_01_standard.jpg',
        },
        {
          src: 'https://assets.adidas.com/images/w_600,f_auto,q_auto/844183a987e24bbfb5daaf5d0115287d_9366/Botines_Predator_Accuracy.3_Sin_Cordones_Terreno_Firme_Negro_GW4597_22_model.jpg',
        },
        {
          src: 'https://assets.adidas.com/images/w_276,h_276,f_auto,q_auto,fl_lossy,c_fill,g_auto/84665150f3ce454084dbacd300f426c0_9366/FY9042_01_standard.jpg',
        },
        {
          src: 'https://assets.adidas.com/images/w_600,f_auto,q_auto/459c0f454f1445aa9cb6af1f00bd2d12_9366/Zapatillas_Adizero_Adios_Pro_3.0_Turquesa_GW4249_01_standard.jpg',
        },
      ],
    }
  },
}

  </script>
  