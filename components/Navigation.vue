<template>
  <section>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container">
        <a class="navbar-brand" href="#"
          ><img src="/Logo.png" alt="logo" class="img-fluid"
        /></a>
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item active">
              <a class="nav-link" href="#"
                >Home <span class="sr-only">(current)</span></a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Dashboard</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Projects</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Tasks</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Reporting</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Users</a>
            </li>
          </ul>
          <div class="right-section">
            <ul class="navbar-nav">
              <li class="nav-item">
                <button class="btn btn-outline-secondary">
                  <img src="/zap.png" alt="" class="img-fluid" />
                  <span>Upgrade Now</span>
                </button>
              </li>
              <li class="nav-item">
                <div class="d-flex">
                  <img
                    src="/gear.png"
                    alt=""
                    class="img-fluid mr-1"
                    role="button"
                  />
                  <img src="/bell.png" alt="" class="img-fluid" role="button" />
                </div>
              </li>
              <li class="nav-item">
                <img src="/avatar.png" alt="" class="img-fluid" role="button" />
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
    <div class="lower-nav py-3 d-none d-md-block">
        <div class="container">
            <div class="d-flex justify-content-between">
        <div class="page-controls">
          <ul class="nav nav-pills">
            <li class="nav-item">
              <a class="nav-link active" href="#">Overview</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Notifications</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Analytics</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Saved reports</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Trade history</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">User reports</a>
            </li>
          </ul>
        </div>
        <div class="search">
          <div class="input-group mb-3">
            <div class="input-group-prepend">
              <span class="input-group-text" id="basic-addon1">
                  <b-icon icon="search"></b-icon>
              </span>
            </div>
            <input
              type="text"
              class="form-control"
              placeholder="Search"
              aria-label="Search"
              aria-describedby="basic-addon1"
            />
          </div>
        </div>
      </div>
        </div>
      
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style>
.right-section li {
  margin-left: 20px;
}

.nav-pills .nav-link.active {
    background: #F9FAFB;
    color: #344054
}

.lower-nav .nav-pills .nav-link {
    color: #344054
}

.search {
    width: 33%;
}

@media (max-width: 427px) {
    .search {
    width: 100%;
}
}
</style>