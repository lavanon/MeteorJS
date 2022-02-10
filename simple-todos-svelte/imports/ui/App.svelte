<script>
  import Task from './Task.svelte';

  const getTasks = () => ([
      { _id: 'task_1', text: 'Do this meteor course' },
      { _id: 'task_2', text: 'Enjoy the process of learning' },
      { _id: 'task_3', text: 'Be # proud' },
  ])
</script>

<div class="container">
  <header>
      <h1>Todo List</h1>
  </header>

  <ul>
      {#each getTasks() as task (task._id)}
          <Task task={task} />
      {/each}
  </ul>
</div>
<!-- 
<div class="container">
  <h1>Welcome to Meteor!</h1>

  <button on:click={addToCounter}>Click Me</button>
  <p>You've pressed the button {counter} times.</p>

  <h2>Learn Meteor!</h2>
  <ul>
    <li><a href="https://svelte-tutorial.meteor.com/" target="_blank">Do the Tutorial</a></li>
    <li><a href="http://guide.meteor.com" target="_blank">Follow the Guide</a></li>
    <li><a href="https://docs.meteor.com" target="_blank">Read the Docs</a></li>
    <li><a href="https://forums.meteor.com" target="_blank">Discussions</a></li>
  </ul>
</div> -->
