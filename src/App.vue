<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <a class="navbar-brand" href="#">Super Store</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
    
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <form class="form-inline my-2 my-lg-0">
          <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
        </form>
      </div>
    </nav>

    <div class="container">
      <div class="row">
        <div class="col-sm-9">
          <div class="row">
            <div class="card" style="width: 13rem;">
              <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRqzNPumeN84ddxOtvpMd93rWlWjLHTbyPH__PaK6tODA&s" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
              </div>
            </div>
            <div class="card" style="width: 13rem;">
              <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRqzNPumeN84ddxOtvpMd93rWlWjLHTbyPH__PaK6tODA&s" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
              </div>
            </div>
            <div class="card" style="width: 13rem;">
              <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRqzNPumeN84ddxOtvpMd93rWlWjLHTbyPH__PaK6tODA&s" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
              </div>
            </div>
          </div>
        </div>
        <div class="col-sm-3">
          <ul class="list-group">
            <li class="list-group-item">
              Item - price
            </li>
            <li class="list-group-item">
              Item - price
            </li>
            <li class="list-group-item">
              Item - price
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container{
  padding: 10px;
}
</style>
