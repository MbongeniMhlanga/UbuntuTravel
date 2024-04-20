<template>
    <div class="flight-list">
      <h2>Available Flights</h2>
      <div v-for="(flight, index) in availableFlights" :key="index" class="flight-card">
        <p><strong>Date:</strong> {{ flight.date }}</p>
        <p><strong>Departure:</strong> {{ flight.departure }}</p>
        <p><strong>Destination:</strong> {{ flight.destination }}</p>
        <p><strong>Departure Time:</strong> {{ flight.departureTime }}</p>
        <p><strong>Arrival Time:</strong> {{ flight.arrivalTime }}</p>
        <p><strong>Available Seats:</strong> {{ flight.availableSeats }}</p>
        <button v-if="flight.availableSeats > 0" @click="book(flight)" class="book-button">Book</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        availableFlights: [
          { date: '2024-04-20', departure: 'O.R Tambo International', destination: 'King Shaka International', departureTime: '09:00 AM', arrivalTime: '12:00 PM', availableSeats: 5 },
          { date: '2024-04-20', departure: 'King Shaka International', destination: 'Cape Town International', departureTime: '11:00 AM', arrivalTime: '02:00 PM', availableSeats: 0 },
          { date: '2024-04-20', departure: 'Cape Town International', destination: 'O.R Tambo International', departureTime: '01:00 PM', arrivalTime: '05:00 PM', availableSeats: 10 },
          // Add more flights here
        ]
      };
    },
    methods: {
      book(flight) {
        const msg = 'Booking successful for ' + flight.departure + ' to ' + flight.destination + '!';
        console.log('Booking:', flight);
        // Example: You may want to send a request to book this flight
        // Example: Decrease the availableSeats for this flight
        flight.availableSeats--; // Decrease available seats by 1
      }
    }
  };
  </script>
  
  <style scoped>
  .flight-list {
    margin-top: 20px;
  }
  
  .flight-card {
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 10px;
    margin-bottom: 15px;
  }
  
  .book-button {
    background-color: #4CAF50; /* Green */
    border: none;
    color: white;
    padding: 10px 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    border-radius: 5px;
    cursor: pointer;
    transition-duration: 0.4s;
  }
  
  .book-button:hover {
    background-color: #45a049;
  }
  </style>
  