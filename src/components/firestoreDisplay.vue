<template>
<div>
  {{ msg }}
  <div>
    <div v-for="(test, key, index) in tests" :key="index">
      <p class="testname">{{test.testname}}</p>
    </div>
  </div>
</div>
</template>

<script>
import db from './firebaseInit'
export default {
  name: 'firestoreDisplay',
  data () {
    return {
      msg: 'firestoreDisplay',
      tests: []
    }
  },
  created () {
      db.collection('tests').get().then((querySnapshot) => {
        querySnapshot.forEach((doc) => {
          let data = {
            'id': doc.id,
            'testname': doc.data().testname
          }
          this.tests.push(data)
          console.log("ああああ")
          console.log("いいいい")
        })
      })
    }
}
</script>

<style scoped>

</style>


