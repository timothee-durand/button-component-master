<template>
  <div id="app">

      <h1>Buttons</h1>

    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ simple }}</code>
        <Button/>
      </div>

      <div class="button-presentation">
        <code class="button-presentation-text">{{ simpleFocusHover }}</code>
        <Button force-hover-focus/>
      </div>
    </div>
    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ outline }}</code>
        <Button variant="outline"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ simpleFocusHover }}</code>
        <Button variant="outline" force-hover-focus/>
      </div>
    </div>
    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ text }}</code>
        <Button variant="text"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ simpleFocusHover }}</code>
        <Button variant="text" force-hover-focus/>
      </div>
    </div>
    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ text }}</code>
        <Button disable-shadow/>
      </div>
    </div>
    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ disabled }}</code>
        <Button disabled/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ disabledText }}</code>
        <Button disabled variant="text"/>
      </div>
    </div>

    <div class="row">

      <div class="button-presentation">
        <code class="button-presentation-text">{{ startIcon }}</code>
        <Button start-icon="local_grocery_store"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ endIcon }}</code>
        <Button end-icon="local_grocery_store"/>
      </div>
    </div>

    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ sm }}</code>
        <Button size="sm"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ md }}</code>
        <Button  size="md"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ lg }}</code>
        <Button  size="lg"/>
      </div>
    </div>

    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ defaultColor }}</code>
        <Button color="default"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ primary }}</code>
        <Button color="primary"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ secondary }}</code>
        <Button color="secondary"/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ danger }}</code>
        <Button color="danger" />
      </div>
    </div>

    <div class="row">
      <div class="button-presentation">
        <code class="button-presentation-text">{{ simpleFocusHover }}</code>
        <Button color="default" force-hover-focus/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ simpleFocusHover }} </code>
        <Button color="primary" force-hover-focus/>
      </div>
      <div class="button-presentation" >
        <code class="button-presentation-text">{{ simpleFocusHover }} </code>
        <Button color="secondary" force-hover-focus/>
      </div>
      <div class="button-presentation">
        <code class="button-presentation-text">{{ simpleFocusHover }} </code>
        <Button color="danger" force-hover-focus/>
      </div>
    </div>

    <div class="row">
      <p class="button-presentation-text">Icons: <a href="Icons: https://material.io/resources/icons/?style=round">https://material.io/resources/icons/?style=round</a></p>
    </div>
    <div class="row">
      <p class="presentation-text">Timothée DURAND  @ DevChallenges.io</p>
    </div>
  </div>
</template>

<script>


import Button from "@/components/Button.vue";

export default {
  name: 'App',
  components: {
    Button

  },
  data() {
    return {
      simple: "<Button/>",
      simpleFocusHover: "&:hover, &:focus",
      outline:"<Button variant='outline'/>",
      text:"<Button variant='text'/>",
      disableShadow:"<Button disable-shadow/>",
      disabled:"<Button disabled/>",
      disabledText:"<Button disabled variant='text'/>",
      startIcon:"<Button start-icon=\"local_grocery_store\"/>",
      endIcon:"<Button end-icon=\"local_grocery_store\"/>",
      sm:"<Button size=\"sm\"/>",
      md:"<Button size=\"md\"/>",
      lg:"<Button size=\"lg\"/>",
      defaultColor:"<Button color=\"default\"/>",
      primary:"<Button color=\"primary\"/>",
      secondary:"<Button color=\"secondary\"/>",
      danger:"<Button color=\"danger\"/>",
    }
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&family=Poppins:wght@500&family=Ubuntu+Mono&display=swap');

root {
  font-size: 62.5%;
}

#app {
  margin: 0;
  padding: 53px 20px 14px 83px;
  display: grid;
}

h1 {
  font-family: Poppins, sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 24px;
  line-height: 36px;
  color: #4F4F4F;
  margin-bottom: 28px;
}

.button-presentation {
  display: flex;
  flex-direction: column;
  margin-right: 155px;
}

.row {
  display: flex;
  margin-bottom: 45px;
}

.button-presentation-text {
  font-family: Ubuntu Mono;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 12px;
  color: #333333;
  margin-bottom: 12px;
}

.presentation-text{
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  color: #A9A9A9;
}
</style>
