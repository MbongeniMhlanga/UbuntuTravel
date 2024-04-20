<template>
  <div class="container">
    <h1>Ubuntu Travel</h1>

    <div class="row">
      <!-- ENTRY FIELD FOR ORIGIN -->
      <div class="mb-3 col-6">
        <label for="basic-url" class="form-label">Origin</label>
        <div class="input-group">
          <span class="input-group-text" id="basic-addon3">Origin</span>
          <input
            type="text"
            class="form-control"
            id="basic-url"
            aria-describedby="basic-addon3 basic-addon4"
          />
        </div>
      </div>

      <!-- ENTERY FIELD FR DESTINATION -->
      <div class="mb-3 col-6">
        <label for="basic-url" class="form-label">Destination</label>
        <div class="input-group">
          <span class="input-group-text" id="basic-addon3">Destination</span>
          <input
            type="text"
            class="form-control"
            id="basic-url"
            aria-describedby="basic-addon3 basic-addon4"
          />
        </div>
      </div>
    </div>
    <!-- CHECK BOX FOR RETURN FLIGHT -->
    <div class="input-group">
      <div class="input-group-text">
        <input
          class="form-check-input mt-0"
          type="radio"
          value=""
          aria-label="Radio button for following text input"
        />
      </div>
      <input
        type="text"
        class="form-control"
        aria-label="Text input with radio button"
      />
    </div>

    <!-- <div class="input-group">
      <div class="input-group-text">
        <input
          class="form-check-input mt-0"
          type="radio"
          value=""
          aria-label="Radio button for following text input"
        />
      </div>
      <input
        type="text"
        class="form-control"
        aria-label="Text input with radio button"
      />
    </div> -->

    <NuxtLink to="/about">About</NuxtLink>
  </div>
  <!-- <button type="button" class="btn btn-secondary">About</button> -->
</template>
