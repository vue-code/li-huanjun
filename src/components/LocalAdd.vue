<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col
          cols="2"
          md="1"
        >  
        <v-text-field
        v-model="aa"
        label="aa"
        ></v-text-field>
        </v-col>

        <v-col
        cols="2"
        md="1"
        > 
        <v-btn>+</v-btn>
        </v-col>

        <v-col
          cols="2"
          md="1"
        >
        <v-text-field
        v-model="bb"
        label="bb"
        ></v-text-field>
        </v-col>
        
        <v-col
        cols="2"
        md="1"
        > 
        <v-btn>=</v-btn>
        </v-col>

        <v-col
          cols="2"
          md="1"
        >  
        <v-text-field
        v-model="ss"
        >
        </v-text-field>
        </v-col>

      </v-row>
        <v-btn @click="add">add</v-btn>
    </v-container>
  </v-form>
</template>

<script>

  export default {
    data: () => ({
      aa: "",
      bb: "",
      ss: ""
    }),
    methods: {
        add () {
            this.ss = Number(this.aa) + Number(this.bb);
        }
    }
  }
</script>
