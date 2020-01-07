<template>
  <v-form v-model="valid">
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

        <v-btn>+</v-btn>

        <v-col
          cols="2"
          md="1"
        >
          <v-text-field
          v-model="bb"
          label="bb"
          ></v-text-field>
        </v-col>
        
        <v-btn>=</v-btn>

        <v-col
          cols="2"
          md="1"
        >  
          <v-text-field
          v-model="ss"
          label="???"
          >
        </v-text-field>
        </v-col>
        <v-btn @click="add">add</v-btn>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>

  export default {
    data: () => ({
      valid: false,
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
