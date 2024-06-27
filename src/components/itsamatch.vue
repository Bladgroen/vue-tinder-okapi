<template>
  <div class="modal-container">
    <div class="overlay"></div>
    <div class="match">
      <img :src="ImgUrl" class="stella" />
      <img src="@/assets/match.png" class="match-image" />
      <h2>€ {{prijs}}</h2>
    </div>
  </div>
</template>

<style scoped>
.modal-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 10000;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent black background */
  z-index: 1;
}

.match {
  position: relative;
  z-index: 2;
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}

.stella {
  display: block;
  width: 500px; /* Fixed width */
  height: 550px; /* Fixed height */
}

.match-image {
  position: absolute;
  top: 25%;
  left: 53%;
  transform: translate(-50%, -50%);
  z-index: 3;
}

h2 {
  margin: 0;
  font-size: 3rem;
}
</style>

<script>
export default {
    props: {
        ImgUrl: {
            type: String,
            required: true
        },
        prijs: {
            type: String,
            required: true
        }
    }
}

</script>
