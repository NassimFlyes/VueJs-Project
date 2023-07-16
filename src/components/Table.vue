<template>
    <table id="t1" class="table table-bordered">
      <thead>
        <tr>
          <th>Player Name</th>
          <th>Player Number</th>
          <th>Player Team</th>
          <th>Action</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(player, index) in players" :key="index">
          <td>{{ player.name }}</td>
          <td>{{ player.number }}</td>
          <td>{{ player.team }}</td>
          <td>
            <button @click="editPlayer(player)" class="btn btn-sm btn-primary">Edit</button>
            <button @click="deletePlayer(index)" class="btn btn-sm btn-danger">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>
  </template>
  
  <script>
  export default {
    data() {
      return {
        players: [
          { name: 'Player 1', number: 10, team: 'Team A' },
          { name: 'Player 2', number: 5, team: 'Team B' },
          { name: 'Player 3', number: 7, team: 'Team C' },
        ]
      };
    },
    methods: {
      editPlayer(player) {
        console.log(`Editing player: ${player.name}`);
      },
      deletePlayer(index) {
        console.log(`Deleting player at index: ${index}`);
        this.players.splice(index, 1);
      }
    }
  };
  </script>
<style>
#t1{
    width: 800px;
    margin: 100px auto;
}
</style>  