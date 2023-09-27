<script>
  import Slider from "./Slider.svelte";
  let redColor = 100;
  let greenColor = 100;
  let blueColor = 100;
</script>

<div class="row">
  <div class="col">
    <h1>Color Picker</h1>
  </div>
</div>
<div class="row">
  <div class="column">
    <form>
      <Slider colorName="Red" bind:colorValue={redColor} />
      <Slider colorName="Green" bind:colorValue={greenColor} />
      <Slider colorName="Blue" bind:colorValue={blueColor} />
    </form>
  </div>
</div>
<div class="row">
  <div class="column">
    <div
      id="color"
      style="background-color: rgb({redColor},
      {greenColor},
      {blueColor})"
    />
  </div>
</div>
<div class="row">
  <div class="column">
    <h2>
      rgb({redColor},
      {greenColor},
      {blueColor})
    </h2>
  </div>
</div>

<style>
  #color {
    height: 300px;
    border: dashed 3px;
  }
  h2 {
    text-align: center;
    text-decoration: underline;
    text-transform: uppercase;
    margin-top: 20px;
  }
</style>
