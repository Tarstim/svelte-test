
  <style>
    .container {
      margin: 50px auto;
      max-width: 800px;
      padding: 0 20px;
    }
  </style>
  
  <script>
</script>
<main>
    <form on:submit|preventDefault={add}>
        <input bind:value={newItem} placeholder="Enter to-do" />
        <button class="add-todo" on:click={add}><span>+</span></button>
      </form>
      
</main>
<style>
    let newItem = '';
let todoList = [];
function add() {
  if (newItem !== '') {
    todoList = [
      ...todoList,
      {
        задача: newItem,
        завершено: false,
      },
    ];
    newItem = '';
  }
}


</style>
