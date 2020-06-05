<template>
    <div>
        {{notes}}
    </div>
</template>

<script>
const urlApi = 'http://localhost:3000/notes';

export default {
  data(){
    return {
      notes: ''
    }
  },
  name: 'Notes',
  created () {
    this.getNotes()
  },
  methods: {
    getNotes () {
      fetch(urlApi, {
        method: 'GET'
      })
        .then(response => {
          return response.json()
        })
        .then(response => {
          this.notes = response
        })
        .catch(err => {
          console.log(err)
        })
    }
  }
};

</script>

<style>

</style>
