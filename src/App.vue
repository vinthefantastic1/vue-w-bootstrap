<template>
  <div id="app">
  <b-container>
    <div class="row">
    <h1>Hello, Bootstrap-Vue</h1>
    </div>

    <b-btn 
      variant="primary"
      @click="showAlert = true"
       v-b-tooltip.hover 
  title="This button triggers the alert"
       >
      Click
    </b-btn>


    <b-alert 
      v-bind:show="showAlert"
      variant="success" >

      You clicked the button!
    </b-alert>

  </b-container>

      <div id="app" class="table table-condensed table-striped">
    <h2>Employees</h2>

    <employee-table />
  </div>
  </div>
</template>

<script>



import EmployeeTable from '@/components/EmployeeTable.vue'

export default {
  name: 'App',
  components: {
    EmployeeTable,
  },
data: () => ({
    showAlert: false
  })


}
</script>


