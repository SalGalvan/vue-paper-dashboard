<template>
  <card class="card-user">
    <div slot="image">
      
    </div>
    <div>
      <div class="author">
       
         
     
        <h4 class="title">
          Sal Galvan
          <br />
          <a href="#">
            <small>On Leave</small>
          </a>
        </h4>
      </div>
      <p class="description text-center">
        
        <br />
        <br />
        
      </p>
    </div>
    <hr />
    <div class="text-center">
      <div class="row">
        <div
          v-for="(info, index) in details"
          :key="index"
          :class="getClasses(index)"
        >
          <h5>
            {{ info.title }}
            <br />
            <small>{{ info.subTitle }}</small>
          </h5>
        </div>
      </div>
    </div>
  </card>
</template>
<script>
export default {
  data() {
    return {
      details: [
        {
          title: "",
          subTitle: "",
        },
        {
          title: "",
          subTitle: "",
        },
        {
          title: "",
          subTitle: "",
        },
      ],
    };
  },
  methods: {
    getClasses(index) {
      var remainder = index % 3;
      if (remainder === 0) {
        return "col-lg-3 offset-lg-1";
      } else if (remainder === 2) {
        return "col-lg-4";
      } else {
        return "col-lg-3";
      }
    },
  },
};
</script>
<style></style>
