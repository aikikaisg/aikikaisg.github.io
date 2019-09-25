<template>
  <div class="about">
    <p>We are the Singapore chapter of the Aikikai Foundation, affiliated to the Aikido World Headquarters, Japan</p>

    <div>
      <img :src="logoImg" alt="Logo Image" class="img-raised rounded-circle img-fluid" />
    </div>

    <br>

    <p>This logo represents Aikikai (Singapore) and embodies its teachings and positive attitudes</p>

    <ul>
        <li>3 petals in light pink signify the Mind, Body and Spirit</li>
        <li>The red circle below signifies "Ki" or "Qi" -inner power produced when the mind, body and spirit unites</li>
        <li>All these formed within a circular structure, as circularity is constant in Aikido</li>
        <li>This logo also resembles an orchid, the national flower of Singapore, while the red circle resembles the rising sun of Japan</li>
        <li>The inseparable formation of the orchid and the red circle signifies a harmonious relationship between Aikikai (Singapore) and Hombu Dojo in Japan</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    logoImg: {
      type: String,
      default: require("@/assets/img/logo.jpg")
    }
  }
};
</script>