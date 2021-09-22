<template>
  <h1>Btn component</h1>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button />' }}</p>
      <CustomBtn text="Default" variant="default"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">&:hover, &:focus</p>
      <CustomBtn text="Default" variant="default" hover="true"/>
    </div>
  </div>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button variant=”outline” />' }}</p>
      <CustomBtn text="Default" variant="outlined"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">&:hover, &:focus</p>
      <CustomBtn text="Default" variant="outlined" hover="true"/>
    </div>
  </div>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button variant=”text” />' }}</p>
      <CustomBtn text="Default" variant="text"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">&:hover, &:focus</p>
      <CustomBtn text="Default" variant="text" hover="true"/>
    </div>
  </div>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button disableShadow />' }}</p>
      <CustomBtn text="Default" variant="default" disable-shadow="true"/>
    </div>
  </div>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button disabled />' }}</p>
      <CustomBtn text="Disabled" disabled="true"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">{{ '<Button variant=”text” disabled />' }}</p>
      <CustomBtn text="Disabled" variant="text" disabled="true"/>
    </div>
  </div>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button startIcon=”local_grocery_store” />' }}</p>
      <CustomBtn text="Default" start-icon="local_grocery_store" color="primary"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">{{ '<Button endIcon=”local_grocery_store” />' }}</p>
      <CustomBtn text="Default" end-icon="local_grocery_store" color="primary"/>
    </div>
  </div>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button size=”sm” />' }}</p>
      <CustomBtn text="Default" size="sm" color="primary"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">{{ '<Button size=”md” />' }}</p>
      <CustomBtn text="Default" size="md" color="primary"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">{{ '<Button size=”lg” />' }}</p>
      <CustomBtn text="Default" size="lg" color="primary"/>
    </div>
  </div>

  <div class="section">
    <div class="btn-section">
      <p class="btn-title">{{ '<Button color=”default” />' }}</p>
      <CustomBtn text="Default"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">{{ '<Button color=”primary” />' }}</p>
      <CustomBtn text="Default" color="primary"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">{{ '<Button color=”secondary” />' }}</p>
      <CustomBtn text="Secundary" color="secondary"/>
    </div>

    <div class="btn-section">
      <p class="btn-title">{{ '<Button color=”danger” />' }}</p>
      <CustomBtn text="Danger" color="danger"/>
    </div>
  </div>

  <div class="section">
    <p class="btn-title">&:hover, &:focus</p>
    <div>
      <div class="btn-section">
        <CustomBtn text="Default" variant="default" hover="true"/>
      </div>

      <div class="btn-section">
        <CustomBtn text="Default" color="primary" hover="true"/>
      </div>

      <div class="btn-section">
        <CustomBtn text="Secundary" color="secondary" hover="true"/>
      </div>

      <div class="btn-section">
        <CustomBtn text="Danger" color="danger" hover="true"/>
      </div>
  </div>
  </div>
</template>

<script>

import CustomBtn from "./components/CustomBtn";

export default {
  name: 'App',
  components: { CustomBtn }
}
</script>

<style lang="scss">
@import './assets/reset.css';

@import url('https://fonts.googleapis.com/css2?family=Ubuntu+Mono&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@500&display=swap');

$primary-color: #333333;
$secundary-color: #4F4F4F;


body {
  padding-left: 25px;
  padding-top: 25px;

  h1 {
    font-family: 'Poppins', sans-serif;
    color: $secundary-color;
    font-size: 24px;
    margin-bottom: 28px;
  }
}

.section {
  display: flex;

  .btn-section {
    margin-right: 75px;
    margin-bottom: 45px;

    .btn-title {
      font-family: 'Ubuntu Mono', sans-serif;
      margin-bottom: 12px;
    }

  }

  &:last-child {
    display: flex;
    flex-direction: column;

    p { margin-bottom: 12px; }
    div { display: flex; }
  }
}
</style>
