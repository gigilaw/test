<template>
  <div class="hello">
    <b-card bg-variant="light">
      <b-form-group
        label-cols-lg="3"
        label="ABC"
        label-size="lg"
        label-class="font-weight-bold pt-0"
        class="mb-0"
      >
        <b-form-group
          label-cols-sm="3"
          v-for="trait in traits"
          :key="trait"
          :label="key"
          label-align-sm="right"
          label-for="nested-street"
        >
          <b-form-input :v-model="trait"></b-form-input>
        </b-form-group>
      </b-form-group>
    </b-card>

    <b-button variant="outline-primary" @click="show">Show</b-button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: function () {
    return {
      traits: {
        firstName: "",
        lastName: "",
        gender: "",
        age: "",
        job: "",
        skinColor: "",
        hairColor: "",
      },
    };
  },
  methods: {
    show: function () {
      console.log(this.traits);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
