<template>
  <div>
    <v-card class="elevation-10 transparent">

        <v-card-text class="text-xs-center">
         <v-img class="white--text elevation-3"  height="170px" :src="imgUrl" ></v-img>
        
        <v-flex xs12 align-end d-flex>
                <span class="headline">{{ title }}</span>
        </v-flex>
            {{ content }}
        </v-card-text>

        <v-card-actions>
            <v-btn color="warning"  v-show="opis" @click="opis=opis">Opis</v-btn>
            <v-spacer></v-spacer>
            <v-btn flat class="blue--text" v-bind:href="gallery">Zobacz więcej</v-btn>
        </v-card-actions>

    </v-card>

  </div>
</template>

<script>
export default {
  props:{
    title: {
      type: String,
      default: ""
    },
    content: "",
    imgUrl: "",
    gallery: "",
    opis: ""
  }
}
</script>
