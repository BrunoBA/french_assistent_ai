<script lang="ts">
export default {
  data() {
    return {
      text: "Patricia se reveille à 06:30 du matin, faire son lit ensuite elle se brosse les dents avec de l´eau chaude et s'abille por faire une randoné de 5 km, elle dit que la donne l'energie necessaire pour la journeé. À 07:30 elle se douche e aprés prende son petite dejeuner, une omelette, des fruits (une banane et des resins) et des tartines (une avec du jambon e une autre avec du fromage) les deux avec de la tomate. Patricia mis 20 min pour lire une livre et ecrir des choses à faire chez-elle. Ensuit elle choise queslque vêtement elle vá utilizer pendant la journeé, se maquille e voilà, Patricia est prêt. Même qu'elle deteste le métro dans les matins elle lui-prende vers 12:30. À 13:00 prend son dejeuner avec ses copins et à 19:00 propose a ses amis d'aller au cinema ou dinêr. Aprés une bonne restaurant, elle arrive chez-elle à 21:00 e prend sa douche à 22:00 après une longue journeé. Patricia se couche très tard à 00:00 en regardent de sa série favorite"
    }
  },
  computed: {
    quantityOfWords() {
      return this.text.trim().split(' ').length
    }
  }
}
</script>

<template>
  <div class="mb-3">
    <label for="exampleFormControlInput1" class="form-label">Titre</label>
    <input
      type="text"
      class="form-control"
      id="exampleFormControlInput1"
      placeholder="Ici votre titre"
    />
  </div>
  <div class="mb-3">
    <label for="exampleFormControlTextarea1" class="form-label">
      Production Écrite
      <small v-if="text.length > 0">({{ quantityOfWords }})</small>
    </label>
    <textarea
      v-model="text"
      spellcheck="false"
      class="form-control"
      id="exampleFormControlTextarea1"
      rows="10"
    ></textarea>
    <small class="ml-2">Pour apprendre plus vite c'est bien avoir min de 160 mots</small>
  </div>
  <button class="btn btn-primary">C'est fini!</button>
</template>
