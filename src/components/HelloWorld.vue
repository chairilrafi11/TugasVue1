<template>
  <div>
    <h1>{{ nama }}</h1>
    <input type="text" v-model="nama">
    <br><br>
    <h2>Nilai Anda : {{ nilai }} </h2>
    <br>    
    <h3>{{ soal1 }}</h3>
    <input type="radio" name="jawaban1" :disabled="checked" > 15
    <input type="radio" name="jawaban1" :disabled="checked" > 9
    <input type="radio" name="jawaban1" :disabled="checked" @click="benar"> 20
    <h3>{{ soal2 }}</h3>
    <input type="radio" name="jawaban2" :disabled="checked2" @click="benar2"> Ridwan Kamil
    <input type="radio" name="jawaban2" :disabled="checked2"> Asep Tapip
    <input type="radio" name="jawaban2" :disabled="checked2"> Edy Rahmayadi
    <h3>{{ soal3 }}</h3>
    <input type="radio" name="jawaban3" :disabled="checked3" > Surat Izin Makan
    <input type="radio" name="jawaban3" :disabled="checked3" @click="benar3"> Surat Izin Mengemudi
    <input type="radio" name="jawaban3" :disabled="checked3" > Surat Izin Maling
  </div>
</template>

<script>
export default {
  name: 'Tugas1',
  data () {
    return {
      nama: 'Nama Anda',
      nilai: 0,
      soal1: '1. Berapa hasil 4 X 5?',
      soal2: '2. Siapa Gubernur Jawa Barat?',
      soal3: '3. Kepanjangan SIM adalah?'
    }
  },
  methods:{
    benar(){
      this.nilai += 1,
      this.checked = true
    },
     benar2(){
      this.nilai += 1,
      this.checked2 = true
    },
     benar3(){
      this.nilai += 1,
      this.checked3 = true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  font-size: 30px;
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
