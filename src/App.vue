<script>
export default {
  name: 'App',
  data() {
    return {
      titulo: "",
      emoji: "",
      apreciacion: "",
      opinion: "",
      competencias: []
    }
  }
}
</script>

<template>
<div class="app">
  <div class="row">
    <div class="col-6">
      <form class="form_derecho" action="">
        <label for="title">Titulo:</label>
        <input type="text" v-model="titulo">
        <hr>

        <label>Emoji:</label>
        <select v-model="emoji">
          <option key="1" value="😀">😀</option>
          <option key="2" value="👍">👍</option>
          <option key="3" value="👎">👎</option>
          <option key="4" value="🤷‍♀️">🤷‍♀️</option>
          <option key="5" value="🤷‍♂️">🤷‍♂️</option>
          <option key="6" value="🙁">🙁</option>
          <option key="7" value="😐">😐</option>
          <option key="8" value="😊">😊</option>
          
        </select>
        <hr>

        <div>
          <label>Apreciación:</label>
          <input v-model="apreciacion" type="radio" name="apreciacion" value="Regular" id="apreciacion1">
          <label for="apreciacion1">Regular</label>
          <input v-model="apreciacion" type="radio" name="apreciacion" value="Bien"id="apreciacion2">
          <label for="apreciacion2">Bien</label>
          <input v-model="apreciacion" type="radio" name="apreciacion" value="Muy bien"id="apreciacion3">
          <label for="apreciacion3">Muy bien</label>
          <input v-model="apreciacion" type="radio" name="apreciacion" value="Increible"id="apreciacion4">
          <label for="apreciacion4">Increible</label>
        </div>
        <hr>

        <div class="row_check">
          <div class="col1 col-4">
            <label for="">Competencias aprendidas:</label>
          </div>
          <div class="col2 col-8">
            <div class="checks">
              <div class="col_a col-6">
                <input v-model="competencias" type="checkbox" name="competencias" value="Morfología de un componente">
                <span>Morfología de un componente</span><br><br>
                <input v-model="competencias" type="checkbox" name="competencias" value="One-Way y Two-Way data binding">
                <span>One-Way y Two-Way data binding</span><br><br>
                <input v-model="competencias" type="checkbox" name="competencias" value="El patrón de diseño MVVM">
                <span>El patrón de diseño MVVM</span><br><br>
              </div>
              <div class="col_b col-6">
                <input v-model="competencias" type="checkbox" name="competencias" value="Directivas">
                <span>Directivas</span><br><br>
                <input v-model="competencias" type="checkbox" name="competencias" value="Estado">
                <span>Estado</span>
              </div>
            </div>
          </div>
        </div>
        <hr>

        <label>Opinión:</label>
        <textarea v-model="opinion"></textarea>
      </form>
    </div>
    
    <div class="col_der col-6">
      <p>{{ emoji }}</p>
      <h3>{{ titulo }}</h3>
      <p>Y me parece {{ apreciacion }}</p>
      <p>He aprendido:</p>
      <p>{{ competencias.join(", ") }}</p>
      <p>Mi opinión hasta ahora del framework es:</p>
      <p>{{ opinion }}</p>
    </div>
  </div>
</div>
</template>

<style>
.app {
  margin: 50px;
}

.form_derecho {
  background-color: #000000;
  color: #fff;
  border-radius: 10px;
  padding: 10px;
}

label {
  margin-right: 10px;
  margin-left: 3px;
}

hr {
  width: 100%;
  border-color: #fff;
}

.radio {
  margin-right: 2px;
}

.row_check {
  display: flex;
}

.col2 {
  display: flex;
}

span {
  margin-left: 2px;
}

.checks {
  display: flex;
}

.col_a, .col_b {
  display: block;
}

textarea {
  width: 100%;
}

.col_der {
  text-align: center;
  border-radius: 5%;
  border: 1px solid #000;
  padding: 10px;
}
</style>
