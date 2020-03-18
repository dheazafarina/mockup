<style>
  .content {
    background: linear-gradient(to top, #F37335, #FDC830);
    height: 15rem;
  }
  .img-carousel {
    margin-top: 35px !important;
    margin-left: 20%;
  }
  .dropdown-divider {
    height: 0;
    margin-top: 5rem;
    overflow: hidden;
    border-top: 4px solid #e65d0d;
    border-radius: 50px;
    width: 10pc;
  }
</style>

<template>
  <div class="content">
    <div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active"  interval="false">
          <div class="card border-light img-carousel" style="width: 15pc;">
            <div class="card-body">
              <h5 class="card-title font-weight-bold">Login</h5>
              <center>
                <div class="dropdown-divider"></div>
              </center>
            </div>
          </div>
        </div>
        <div class="carousel-item" interval="false">
          <div class="card border-light img-carousel" style="width: 15pc;">
            <div class="card-body">
              <h5 class="card-title font-weight-bold">Discover</h5>
              <center>
                <div class="dropdown-divider"></div>
              </center>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>