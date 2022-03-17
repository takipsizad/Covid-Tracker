<template>
  <select @click="onChange" 
   v-model="selected" class="form-select mt-5 block w-full border p-3 rounded">
    <option value="0">Select</option>
    <option v-for="country in countries" :value="country.ID">
       {{ country.Country }}
       </option>
  </select>
</template>

<script>
export default {
  naem: 'CountrySelect',
  props: ['countries'],
  data(){
      return{
          selected : 0,
      }
  },
  methods:{
      onChange(){
          const country = this.countries.find((item) => item.ID === this.selected)

          this.$emit('get-country', country)
      },
  }
}
</script>

<style>

</style>