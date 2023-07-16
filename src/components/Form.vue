<template>
    <div>
      <h2>Add New Player</h2>
      <form @submit.prevent="addPlayer" class="player-form">
        <div class="form-group">
          <input type="text" placeholder="Player Name" class="form-control" id="playerName" v-model="playerName" required>
        </div>
        <div class="form-group">
          <input type="number" placeholder="Player Number" class="form-control" id="playerNumber" v-model="playerNumber" required>
        </div>
        <div class="form-group">
          <input type="text" placeholder="Player Team" class="form-control" id="playerTeam" v-model="playerTeam" required>
        </div>
        <button type="submit" class="btn btn-primary">Add Player</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        playerName: '',
        playerNumber: '',
        playerTeam: ''
      };
    },
    methods: {
      addPlayer() {
        this.$emit('playerAdded', {
          name: this.playerName,
          number: this.playerNumber,
          team: this.playerTeam
        });
        
        this.playerName = '';
        this.playerNumber = '';
        this.playerTeam = '';
      }
    }
  };
  </script>
  
  <style>
  
  .player-form {
    max-width: 500px;
    padding: 20px;
    margin: 50px auto;
    border: 1px solid #ccc;
    border-radius: 15px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); 
  }
  h2{
    font-family: Georgia, 'Times New Roman', Times, serif;
    margin: 50px auto;
  }
  
  </style>
  