<template>
  <section class="container">
    <app-logo/>
    <div class="about">
      <table>
        <tr><td class="label">Name:</td><td>Chris L Kimball</td></tr>
        <tr><td class="label">DOB:</td><td>06.19.81</td></tr>
        <tr><td class="label">Height:</td><td>2.1 meters</td></tr>
        <tr><td class="label">Weight:</td><td>24 Stones</td></tr>
        <tr><td class="label">Blood type:</td><td>B positive</td></tr>
        <tr><td class="label">Fighting Style:</td><td>Staggered Bear</td></tr>
        <tr><td class="label">Favoite Foods:</td><td>Fried Clams, Pizza, cheese, bread</td></tr>
        <tr><td class="label">Favorites Games:</td><td>Psychonauts (vg), War of the Ring (bg) Gears of War (vg)</td></tr>
        <tr><td></td><td></td></tr>
        <tr><td class="label">Bio:</td><td>Determined to Art from an early age, Chris has undergone an intensive training routine of holding a pencil and making marks on paper... alot! Although after a tragic accident involving a pad of bristol board and some  Sharpies left 17 dead, Chris learned that he must only use his powers of Art for good (and profit). Currently Chris wages war on the forces of darkness as the world�s only freelance, giant, crime-solving, (martial) artist.</td></tr>
        <tr><td class="label">Moves:</td><td>Under Cut [F,F/D,D, P], Temple Crush (throw) (P+K+G+F ,tap P], Halo Rage (against wall) [B+Punch] , Ankle Damage [hold D, K]</td></tr>
      </table>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import AppMenu from '~/components/AppMenu.vue'

export default {
  components: {
    AppLogo,
    AppMenu
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Merriweather:400,700');
@import "~/assets/less/app.less";

.about {
	color: #fff;
	text-align: left;
	padding: 40px 100px;
}

label, .label {
  font-weight: 600;
  margin-right: 15px;
  color: #ae4;
  min-width: 160px;
  vertical-align: top;
}
</style>
