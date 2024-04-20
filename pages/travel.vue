<template>
    <div class="flight-list">
      <div class="travel-heading">
        <h2>Available Flights</h2>
        <div class="flights-question">
            <h3>Choose a departuring point:</h3>
            <select>
                <option value="1">O.R Tambo International</option>
                <option value="2">Cape Town International</option>
                <option value="3">King Shaka International</option>
            </select>
        </div>
      </div>
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
    const ORT = 'O.R Tambo International';
    const CPT = 'Cape Town International';
    const DUR = 'King Shaka International';

    export default {
        data() {
            return {
                availableFlights: [
                { date: '02/11/2024', departure: ORT, destination: 'King Shaka International', departureTime: '09:00 AM', arrivalTime: '12:00 PM', availableSeats: 5 },
                { date: '2024-04-20', departure: CPT, destination: 'Cape Town International', departureTime: '11:00 AM', arrivalTime: '02:00 PM', availableSeats: 0 },
                { date: '05/05/2024', departure: ORT, destination: 'King Shaka International', departureTime: '09:00 AM', arrivalTime: '12:00 PM', availableSeats: 5 },
                { date: '2024-04-20', departure: DUR, destination: 'o.r tambo international', departuretime: '01:00 pm', arrivaltime: '05:00 pm', availableseats: 10 },
                { date: '07/10/2024', departure: ORT, destination: 'King Shaka International', departureTime: '09:00 AM', arrivalTime: '12:00 PM', availableSeats: 5 },
                // Add more flights here
                ]
            };
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

  .travel-heading {
    display: flex;
    flex-direction: row;
    width: auto;
    justify-content: space-between;
    align-items: center;
  }

  .flights-question {
    display: flex;
    flex-direction: column;
    width: auto;
    margin: 10px 0;
  }
  </style>
  