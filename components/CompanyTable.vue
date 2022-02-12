<template>
  <div class="container">
    <b-table-simple responsive outlined class="table-box">
      <b-thead>
        <b-tr>
          <b-th colspan="5">
            <img src="/Checkbox.png" alt="" class="img-fluid mr-1" />
            Company <b-icon icon="arrow-down" class="ml-2"></b-icon>
          </b-th>
          <b-th></b-th>
          <b-th>License Use</b-th>
          <b-th>Status</b-th>
          <b-th>Users</b-th>
          <b-th></b-th>
          <b-th>About</b-th>
          <b-th></b-th>
        </b-tr>
      </b-thead>
      <b-tbody>
        <b-tr v-for="(company, index) in companyData" :key="index">
          <b-td colspan="4">
            <div class="d-flex align-items-center">
              <img :src="`/${company.check}.png`" alt="" class="img-fluid mr-1" />
              <img :src="`/${company.logo}.png`" alt="" class="img-fluid" />
              <div class="ml-2">
                <p class="mb-0" style="color: #101828; font-size: 14px">
                  {{ company.name }}
                </p>
                <p class="mb-0" style="font-size: 14px; color: #667085">
                  {{ company.subName }}
                </p>
              </div>
            </div>
          </b-td>
          <b-td></b-td>
          <b-td></b-td>
          <b-td>
            <div class="progress">
              <div
                class="progress-bar"
                role="progressbar"
                :style="`width: ${company.licenseProgress}%`"
                :aria-valuenow="`${company.licenseProgress}`"
                aria-valuemin="0"
                aria-valuemax="100"
              ></div>
            </div>
          </b-td>
          <b-td>
            <span class="badge badge-pill badge-primary">Primary</span>
          </b-td>
          <b-td class="users-box" colspan="2">
            <div>
              <img src="/user1.png" alt="" class="img-fluid user" />
              <img src="/user1.png" alt="" class="img-fluid user" />
              <img src="/user1.png" alt="" class="img-fluid user" />
              <img src="/user1.png" alt="" class="img-fluid user" />
            </div>
          </b-td>
          <b-td>
            <p class="mb-0" style="color: #101828; font-size: 14px">
              {{ company.aboutOne }}
            </p>
            <p class="mb-0" style="font-size: 14px; color: #667085">
              {{ company.aboutTwo }}
            </p>
          </b-td>
          <b-td>
            <b-icon icon="trash" class="mr-3" role="button"></b-icon>
            <b-icon icon="pencil" role="button"></b-icon>
          </b-td>
        </b-tr>
      </b-tbody>
      <b-tfoot>
        <b-tr>
          <b-td colspan="12">
            <div class="d-none d-md-block">
               <div class="d-flex align-items-center justify-content-between">
              <div>
                <button class="btn grey-outline-btn">Previous</button>
                <button class="btn grey-outline-btn">Next</button>
              </div>
              <div>
                <p class="mb-0">Page 1 of 10</p>
              </div>
            </div>
            </div>
          </b-td>
        </b-tr>
      </b-tfoot>
    </b-table-simple>
    <div class="mt-3 d-md-none d-block">
      <div class="d-flex justify-content-between align-items-center py-3">
        <b-icon icon="arrow-left"></b-icon>
        <p class="mb-0">Page 1 of 10</p>
        <b-icon icon="arrow-right"></b-icon>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      companyData: [
        {
          logo: 'company1',
          name: 'Catalog',
          subName: 'catalogapp.io',
          licenseProgress: 85,
          status: 'Customer',
          aboutOne: 'Content curating app',
          aboutTwo: 'Brings all your news into one Place',
          check: 'Checkbox'
        },
        {
          logo: 'circooles',
          name: 'Circooles',
          subName: 'getcircooles.com',
          licenseProgress: 80,
          status: 'Churned',
          aboutOne: 'Design software',
          aboutTwo: 'Super lightweight design app',
          check: 'Checkbox'
        },
        {
          logo: 'commandr',
          name: 'Command+R',
          subName: 'cmdr.ai',
          licenseProgress: 45,
          status: 'Customer',
          aboutOne: 'Data prediction',
          aboutTwo: 'AI and machine learning data',
          check: 'Checkbox'
        },
        {
          logo: 'hourglass',
          name: 'Hourglass',
          subName: 'hourglass.app',
          licenseProgress: 90,
          status: 'Customer',
          aboutOne: 'Productivity',
          aboutTwo: 'Time management and productivity',
          check: 'unchecked'
        },
        {
          logo: 'layers',
          name: 'Layers',
          subName: 'getlayers.io',
          licenseProgress: 40,
          status: 'Churned',
          aboutOne: 'Web app integrations',
          aboutTwo: 'Connect web apps seamlessly',
          check: 'unchecked'
        },
        {
          logo: 'quotient',
          name: 'Quotient',
          subName: 'quotient.co',
          licenseProgress: 30,
          status: 'Customer',
          aboutOne: 'Sales CRM',
          aboutTwo: 'Web-based sales doc management',
          check: 'Checkbox'
        },
        {
          logo: 'sisyphus',
          name: 'Sisyphus',
          subName: 'sisyphus.com',
          licenseProgress: 50,
          status: 'Customer',
          aboutOne: 'Automation and workflow',
          aboutTwo: 'Time tracking, invoicing and expenses',
          check: 'Checkbox'
        },
      ],
    }
  },
}
</script>

<style>
.progress {
  height: 0.5rem;
}

.users-box {
  position: relative;
}

.users-box .user {
  position: absolute;
}

.users-box .user:nth-child(1) {
  left: 6px;
  top: 20px;
}

.users-box .user:nth-child(2) {
  left: 27px;
  top: 20px;
}

.users-box .user:nth-child(3) {
  left: 48px;
  top: 20px;
}
.users-box .user:nth-child(4) {
  left: 68px;
  top: 20px;
}

.table td {
  vertical-align: middle;
}

@media (min-width: 760px) {
  .table-box {
    background: #ffffff;
    /* Gray/200 */

    border: 1px solid #eaecf0;
    box-sizing: border-box;
    box-shadow: 0px 4px 8px -2px rgba(16, 24, 40, 0.1),
      0px 2px 4px -2px rgba(16, 24, 40, 0.06);
    border-radius: 8px;
  }
}
</style>