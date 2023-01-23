<script>
export default {
  data(){
    return{
      datasensor: "90",
      datasensor2: "80",
    };
  },
  created(){
    //this.getData()
  },
  methods:{
    async getData() {
      const data = await  fetch("http://localhost/sensor")
      const datajson = await data.json()
      this.datasensor = datajson.sensor1
    },
  },
};

</script>

<template>
  
  <div class="flex flex-row gap-x-1">
  <div class="basis-1/4"><button @click="getData" class="bg-green-500 px-2 rounded-full">Tombol</button></div>
  <div class="basis-3/4 border w-40"> Suhu= {{ datasensor }}</div>
  </div>
  <header>
    
  </header>

  <main>
    
  </main>
</template>


