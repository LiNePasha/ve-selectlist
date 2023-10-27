<script setup>
import VueSelectList from 've-selectlist'
import "ve-selectlist/dist/VueSelectList.css"
</script>

<template>
  <div>
    <VueSelectList  :data="categories" optionText="category_name" title="Select Category" @update="onCategriesUpdate" />
  </div>
</template>

<script>
export default {
  components: {
    VueSelectList
  },
  data(){
  return {
    categories: [
            {
                id: 3,
                company_id: 1,
                category_name: "jjjjj"
            },
            {
                id: 4,
                company_id: 1,
                category_name: "new main"
            }
        ],
        category_id: "",
  }
},
methods: {
  onCategriesUpdate(opject) {
    this.category_id = opject.id
  }
}
}
</script>
