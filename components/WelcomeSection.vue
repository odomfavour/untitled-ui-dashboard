<template>
  <div class="container">
    <div class="d-flex justify-content-between flex-md-row flex-column mt-4">
      <div>
        <h1>Welcome back, Olivia</h1>
        <p>Track, manage and forecast your customers and orders.</p>
      </div>
      <div>
        <button class="btn grey-outline-btn">
          <img src="/upload-cloud.png" alt="" class="img-fluid" />
          Import
        </button>
        <button class="btn primary-btn">
          <b-icon icon="plus"></b-icon>Add
        </button>
      </div>
    </div>
    <div class="mt-4">
      <div class="row">
        <div
          class="col-md-4 mb-3"
          v-for="(item, index) in dashboardInfo"
          :key="index"
        >
          <b-card>
            <div class="d-flex justify-content-between align-content-center">
              <p class="mb-0">Total Customers</p>
              <b-icon icon="three-dots-vertical" class="mt-1"></b-icon>
            </div>
            <div class="mt-3">
              <div class="row">
                <div class="col-md-7 col-8">
                  <h2>{{ item.count }}</h2>
                  <div class="mt-3">
                    <b-icon :icon="item.icon" :variant="item.variant"></b-icon>
                    <span class="text-success">{{ item.percent }}%</span> vs
                    last month
                  </div>
                </div>
                <div class="col-md-5 col-4">
                  <img
                    :src="`/${item.img}.png `"
                    alt=""
                    class="img-fluid mt-3"
                  />
                </div>
              </div>
            </div>
          </b-card>
        </div>
      </div>
    </div>
    <div class="mt-3">
        <div class="d-flex justify-content-between align-items-center flex-md-row flex-column">
            <div class="left-section order-md-1 order-2">
                <div class="d-flex flex-md-row flex-column">
                     <div class="order-2 order-md-1">
                    <button class="btn purple-outline-btn mr-2 mb-3 ">All time X</button>
                <button class="btn purple-outline-btn mr-2 mb-3">US, AU +4 X</button>
                </div>
                
                <button class="btn grey-outline-btn mb-3 filter-btn order-1 order-md-2"><b-icon icon="filter"></b-icon> More Filters</button>
                </div>
            </div>
            <div class="search order-md-2 order-1">
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
</template>

<script>
export default {
  data() {
    return {
      dashboardInfo: [
        {
          count: '2,420',
          name: 'Total Customers',
          percent: 40,
          icon: 'arrow-up',
          img: 'green-chart',
          variant: 'success',
          textColor: 'text-success',
        },
        {
          count: '1,210',
          name: 'Members',
          percent: 10,
          icon: 'arrow-down',
          img: 'red-chart',
          variant: 'danger',
          textColor: 'text-danger',
        },
        {
          count: '316',
          name: 'Active now',
          percent: 20,
          icon: 'arrow-up',
          img: 'green-chart',
          variant: 'success',
          textColor: 'text-success',
        },
      ],
    }
  },
}
</script>

<style>
.primary-btn {
  color: #fff;
  background: #7F56D9;
border: 1px solid #7F56D9;
box-sizing: border-box;
font-weight: 500;
font-size: 14px;
box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
border-radius: 8px;
}

.purple-outline-btn {
    background: #F9F5FF;
border: 1px solid #F9F5FF;

box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
border-radius: 8px;
color: #6941C6;
font-weight: 500;
font-size: 14px;
}

.grey-outline-btn {
    background: #FFFFFF;

border: 1px solid #D0D5DD;
box-sizing: border-box;
box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
border-radius: 8px;
color: #344054;
font-size: 14px;
}

@media (max-width: 427px) {
    .filter-btn {
        width: 100%;
    }

    .left-section {
        width: 100%;
    }
}
</style>