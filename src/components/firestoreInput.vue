<template>
<div>
{{ msg }}
<form @submit.prevent="saveContact">
<input type="text" v-model="testname">
<button type="submit">送信</button>
</form>
</div>
</template>

<script>
import db from './firebaseInit'
export default {
  name: 'firestoreInput',
  data () {
    return {
      msg: 'firestoreInput',
      testname: null
    }
  },
  methods: {
    saveContact () {
      db.collection('tests').add({
        testname: this.testname
      }).then(function (docRef) {
        console.log('Document written with ID: ', docRef.id);
      }).catch(function (error) {
        console.error('Error adding document: ', error);
      });
    }
  }
}
</script>

<style scoped>

</style>
