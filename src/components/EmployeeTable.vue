<template>
    <div id="employee-table">
      <table>
        <thead>
          <tr>
            <th>Employee name</th>
            <th>Employee email</th>
            <th>Actions</th> 
          </tr>
        </thead>
        <tbody>
          <tr v-for="(employee, index) in employees" :key="index">
            <td>{{ employee.name }}</td>
            <td>{{ employee.email }}</td>
            <td>
              <button @click="editEmployee(index)">Edit</button>
              <button @click="deleteEmployee(index)">Delete</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    name: 'EmployeeTable',
    props: {
      employees: {
        type: Array,
        required: true
      }
    },
    methods: {
      editEmployee(index) {
        console.log('Editar empleado:', this.employees[index]);
      },
      deleteEmployee(index) {
        console.log('Eliminar empleado:', this.employees[index]);
      }
    }
  }
  </script>
  
  <style scoped>
  </style>
  