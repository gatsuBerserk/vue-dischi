<template>
  <div> 
    <div class="card mb-3 my-color text-white" style="max-width: 540px;">
      <div class="row g-0">
          <div class="col-md-4 p-3">
            <img src="#" class="img-fluid rounded-start" alt="...">
          </div>
          <div class="col-md-8">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
            </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default { 
    name : "DiscPage", 
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/my-style.scss"; 

  .my-color{
    background-color: rgb(46, 58, 70);
  }

</style>