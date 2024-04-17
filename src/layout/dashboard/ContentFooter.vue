<template>
  <footer class="footer">
    <div class="container-fluid d-flex flex-wrap justify-content-between">
      <nav>
        <ul>
          <li>
            <router-link :to="{ path: '/admin' }">Dashboard</router-link>
          </li>
        </ul>
      </nav>
      <div class="">
        &copy; 
        <i class=""></i>
        <a href="https://github.com/cristijora" target="_blank">
          &nbsp; </a
        >&nbsp; 
        <a href="https://www.creative-tim.com/?ref=pdf-vuejs" target="_blank"
          >&nbsp;</a
        >
      </div>
    </div>
  </footer>
</template>
<script>
export default {};
</script>
<style></style>
