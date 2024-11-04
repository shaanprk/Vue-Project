<script>
  export default {
    data: () => ({
          message: 'The order of Straw Hat Pirates',
          strawhats: [
            {
              name: "Luffy",
              bounty: 3000000000
            },
            {
              name: "Zoro",
              bounty: 1111000000
            },
            {
              name: "Nami",
              bounty: 366000000
            },
            {
              name: "Usopp",
              bounty: 500000000
            },
            {
              name: "Sanji",
              bounty: 1032000000
            },
            {
              name: "Chopper",
              bounty: 1000
            },
            {
              name: "Robin",
              bounty: 930000000
            },
            {
              name: "Franky",
              bounty: 394000000
            },
            {
              name: "Brook",
              bounty: 383000000
            },
            {
              name: "Jinbe",
              bounty: 1100000000
            }
          ],
          favoriteList: []
        }),
        methods: {
          addToFavorites(character) {
            this.favoriteList.push(character)
          },
          incrementCount() {
            this.count++
          }
        }
  }
</script>

<template>
  <h2>Straw Hat Pirates</h2>
  <ol>
    <li v-for="character in strawhats">
      {{ character.name }} - {{ character.bounty }}
      <button @click="addToFavorites(character.name)">
        Favorite
      </button>
    </li>
  </ol>

  <h2>Favorite Straw Hat Pirates</h2>
  <ol>
    <li v-for="favchar in favoriteList">{{ favchar }}</li>
  </ol>
</template>