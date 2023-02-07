<template>
  
    <div
      v-motion
      :initial="{ opacity: 0, y: -100 }"
      :visible="{ opacity: 1, y: 0 }"
      :delay="100"
      class="proj"
    >
      <h1>{{data.title}}</h1>
      <a
        :href="data.href"
        target="_blank"
      >
        <div class="projects-img">
          <img
            :src="data.img"
            :alt="data.title"
          />
          <div class="layer">
            <h3>View</h3>
          </div>
        </div>
      </a>
    </div>

</template>


<script>
export default{
    props :{
        data: {
            require: true,
            type: Object,
        }
    },

    data(){
        return{

        }
    }
}
</script>
