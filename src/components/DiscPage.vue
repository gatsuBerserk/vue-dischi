<template>
    <div class="card mb-3 my-color text-white m-3" style="max-width: 540px;">
      <div class="row g-0">
          <div class="col-md-4 p-3">
            <img :src="discObject.poster" class="img-fluid rounded-start" alt="discObject.author">
          </div>
          <div class="col-md-8">
            <div class="card-body text-white">
              <h5 class="card-title fw-bold">{{discObject.title}}</h5>
              <p class="card-text fst-italic">{{discObject.author}}</p>
              <p class="card-text">{{discObject.genre}}</p>
              <p class="card-text">{{discObject.year}}</p>
            </div>
          </div>
      </div>
    </div>
</template>

<script>
export default { 
    name : "DiscPage", 
    props: ["discObject"], 
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/my-style.scss"; 

  div.my-color{
    background-color: rgb(46, 58, 70);
  }

</style>