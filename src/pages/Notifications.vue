<template>
  
    <div>
      <div class="row">
        <div class="col-md-6">
          <h5>Recent Notifications</h5>
          <div class="alert alert-info">
            <button type="button" aria-hidden="true" class="close">×</button>
            <span>Sal Galvan is on leave.</span>
          </div>
          <div class="alert alert-info">
            <button type="button" aria-hidden="true" class="close">×</button>
            <span>Ric Jimenez was Recently added.</span>
          </div>
          <div class="alert alert-info">
            <button type="button" aria-hidden="true" class="close">×</button>
            <span>5 new colleagues were added.</span>
          </div>
         
        </div>
        <div class="col-md-6">
        
          <div>
            <h5>
             
              <p class="category"></p>
            </h5>
          </div>
        </div>
        
       
            >
          </div>
        </div>
      </div>
    </div>
  </card>
</template>
<script>
import NotificationTemplate from "./Notifications/NotificationTemplate";

export default {
  data() {
    return {
      type: ["", "info", "success", "warning", "danger"],
      notifications: {
        topCenter: false,
      },
    };
  },
  methods: {
    notifyVue(verticalAlign, horizontalAlign) {
      const color = Math.floor(Math.random() * 4 + 1);
      this.$notify({
        component: NotificationTemplate,
        icon: "ti-gift",
        horizontalAlign: horizontalAlign,
        verticalAlign: verticalAlign,
        type: this.type[color],
      });
    },
  },
};
</script>
<style></style>
