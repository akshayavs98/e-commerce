<template>
  <div class="about-container">
    <div class="about-content">
      <div class="description">
        <h2>About Us</h2>
        <p>
          We are a team of passionate individuals committed to delivering the best services to our
          customers. Our mission is to provide high-quality products and create value for our
          clients.
        </p>
        <p>
          Our journey began in 2010, and since then we have grown into a trusted name in the
          industry, continuously innovating and adapting to the needs of our clients.
        </p>
      </div>
      <div class="image-container">
        <img src="@/assets/images/shopping.jpg" alt="About Us" />
      </div>
    </div>
  </div>
</template>

<style>
.about-container {
  max-width: 1200px;
}

.about-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.description {
  flex: 1;
  padding: 20px;
}

.image-container {
  flex: 1;
}

.image-container img {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
}
</style>
