import jsonData from '@/data/data.json';

<template>
    <div>
      <h1>Travel</h1>
      <FlightList :data="data" />
      <table>
        <thead>
          <tr>
            <th>Flight No</th>
            <th>Airline Name</th>
            <th>Departure Place</th>
            <th>Departure Time</th>
            <th>Arrival Place</th>
            <th>Arrival Time</th>
            <th>Price</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in data" :key="item.flightNo">
            <td>{{ item.flightNo }}</td>
            <td>{{ item.airlineName }}</td>
            <td>{{ item.departurePlace }}</td>
            <td>{{ item.departureTime }}</td>
            <td>{{ item.arrivalPlace }}</td>
            <td>{{ item.arrivalTime }}</td>
            <td>{{ item.price }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  import FlightList from './FlightList.vue'; // Import FlightList component
  import jsonData from '@/data/data.json'; // Import JSON data
  
  export default {
    components: {
      FlightList
    },
    data() {
      return {
        data: [] // Initialize data as an empty array
      };
    },
    mounted() {
      // Simulate fetching data from external source
      // Replace this with your actual fetch request
      // fetch('/', {
      //   method: 'GET',
      //   headers: {
      //     'Content-Type': 'application/json',
      //   }
      // })
      // .then(response => response.json())
      // .then(data => {
      //   this.data = data; // Assign fetched data to the component data
      // })
      // .catch(error => {
      //   console.error('Error fetching data:', error);
      // });
      
      // Simulated data processing (replace with actual data processing)
      this.data = jsonData.map(item => ({
        flightNo: item.flightNo,
        airlineName: item.airlineName,
        departurePlace: item.departurePlace,
        departureTime: item.departureTime,
        arrivalPlace: item.arrivalPlace,
        arrivalTime: item.arrivalTime,
        price: item.price
      }));
    }
  };
  </script>
  