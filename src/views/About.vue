<template>
  <div>
    {{ chekboxTodos }}
    {{ select1 }}
    <p></p>
    <input
      type="checkbox"
      id="checkbox"
      value="uno"
      v-model="chekboxTodos"
      @input="addSelect(selectSelect1)"
    />
    <label for="Uno">Uno</label>
    <div>
      <select v-model="select1[0]">
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
        <option value="mercedes">Mercedes</option>
        <option value="audi">Audi</option>
      </select>
    </div>
    <input type="checkbox" id="checkbox2" value="dos" v-model="chekboxTodos" />
    <label for="Dos">Dos</label>
    <div>
      <select v-model="select1[1]">
        <option value="sss" selected>Volvo</option>
        <option value="saab">Saab</option>
        <option value="mercedes">Mercedes</option>
        <option value="audi">Audi</option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  name: "Prueba",
  data() {
    return {
      chekboxTodos: [],
      select1: ["volvo"],
    };
  },
  methods: {
    addSelect(select) {
      return select;
    },
  },
};
</script>

<style></style>
