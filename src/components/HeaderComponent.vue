<template>
  <header>
    <div></div>
    <div class="searchNavigation">
      <h1>BoolFlix</h1>
      
      <ul>
        <li><a href="">Film</a></li>
        <li><a href="">Serie</a></li>
        <li><a href="">La mia lista</a></li>
      </ul>
      <div class="searchbar">
        <input type="text" placeholder="Cerca il tuo Film..." v-model="insertText" @keyup.enter="$emit('textToSearch', insertText)">
        <button @click="$emit('textToSearch', insertText)">Cerca!</button>
    </div>
    </div>
  </header>
</template>

<script>
export default {
name : 'HeaderComponent',
data(){
    return{
        insertText : '',
    }
}
}
</script>

<style lang="scss" scoped>

  header{
    background-color: black;
  }
.searchNavigation{
  display: flex;
  justify-content: space-between;
  align-items: center;
  h1{
    color: #E3170A;
    padding: 15px;
    font-size: 3rem;
  };

  ul{
    color: white;
    list-style-type: none;
    display: flex;
  }

  ul li {
    margin: 15px;
  }
  
  a {
    text-decoration: none;
    color: white;
  }

  input{
    border: none;
    padding: 5px;
    border-radius: 5px; 
    margin-right: 10px;
  };
  button{
    background-color: red;
    border: none;
    padding: 5px;
    border-radius: 5px;
  }
}
.searchbar{
  padding: 0 15px;
}
</style>