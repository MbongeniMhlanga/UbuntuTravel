<template>
  <div class="container">
    <h1>Ubuntu Travel</h1>

    <div class="row">
      <!-- ENTRY FIELD FOR ORIGIN -->
      <div class="mb-3 col-6">
        <label for="basic-url" class="form-label">Origin</label>
        <div class="input-group">
          <span class="input-group-text" id="basic-addon3">Origin</span>
          <select class="form-select" aria-label="Default select example">
            <option value="1">O.R Tambo International</option>
            <option value="2">Cape Town International</option>
            <option value="3">King Shaka International</option>
          </select>
        </div>
      </div>

      <!-- ENTERY FIELD FR DESTINATION -->
      <div class="mb-3 col-6">
        <label for="basic-url" class="form-label">Destination</label>
        <div class="input-group">
          <span class="input-group-text" id="basic-addon3">Destination</span>
          <select class="form-select" aria-label="Default select example">
            <option value="1">O.R Tambo International</option>
            <option value="2">Cape Town International</option>
            <option value="3">King Shaka International</option>
          </select>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-6">
        <div class="input-group mb-3 row">
          <label class="form-label col-2"> From </label>

          <input
            type="date"
            class="form-control offset-1"
            placeholder="Recipient's username"
            aria-label="Recipient's username"
            aria-describedby="basic-addon2"
          />
        </div>
      </div>
      <div class="col-6">
        <div class="input-group mb-3 row">
          <label class="form-label col-2"> To </label>

          <input
            type="date"
            class="form-control offset-1"
            placeholder="Recipient's username"
            aria-label="Recipient's username"
            aria-describedby="basic-addon2"
          />
        </div>
      </div>
    </div>

    <div class="input-group mb-3">
      <label> To </label>

      <input
        type="date"
        class="form-control"
        placeholder="Recipient's username"
        aria-label="Recipient's username"
        aria-describedby="basic-addon2"
      />
    </div>

    <NuxtLink to="/about">About</NuxtLink>
    <div>
      <button class="btn btn-outline-primary">
        <NuxtLink to="/travel">Book</NuxtLink>
      </button>
    </div>
  </div>
  <!-- <button type="button" class="btn btn-secondary">About</button> -->
</template>
