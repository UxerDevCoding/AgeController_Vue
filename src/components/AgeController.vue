<template>
  <div>
    <h2>Age Controller</h2>
    <input type="text" placeholder="Escribe tu edad" id="ageInput" required />
    <button v-on:click="userAge()">Comprobar edad</button>
    <div id="ageController"></div>
  </div>
</template>

<script>
export default {
  name: "AgeController",
  data: () => ({}),

  methods: {
    userAge() {
      let age = parseInt(document.getElementById("ageInput").value);
      let printResult = document.getElementById("ageController");
      printResult.innerHTML = "<p>";
      if (age) {
        if (age >= 18) {
          printResult.innerHTML += "Tienes " + age + " años y puedes conducir";
          return;
        }

        printResult.innerHTML +=
          "Tienes " + age + " años y no tienes permitido conducir";
        return;
      }

      printResult.innerHTML += "Debes introducir tu edad";
    },
  },
};
</script>

<style>
.v-main__wrap {
  display: flex;
  max-width: 100%;
  justify-content: center;
  align-items: center;
  margin-bottom: 60px;
}

.v-main {
  background-color: #e3e6f1;
}

#ageInput {
  display: inline-flex;
  background-color: #ffffff;
  align-items: center;
  border-radius: 0.5rem;
  overflow: hidden;
  font-size: 1rem;
  font-family: "Lucida Sans Regular";
  box-shadow: 0px 2px 4px 1px rgba(141, 141, 141, 0.5);
  padding: 10px;
}

button {
  padding: 10px;
  background-color: rgb(59, 212, 212);
  margin-left: 10px;
  font-size: 1rem;
  border-radius: 0.5rem;
  font-family: "Lucida Sans";
  font-weight: bold;
  box-shadow: 0px 2px 4px 1px rgba(0, 0, 0, 0.25);
}

h2 {
  margin-bottom: 60px;
  text-align: center;
  font-family: "Lucida Sans Regular";
}

* {
  padding: 0;
  margin: 0;
  justify-content: center;
  align-content: center;
  text-align: center;
}

#ageController {
  margin-top: 30px;
  font-family: "Lucida Sans Regular";
}
</style>
