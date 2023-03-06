<script>
  import Button from "../../components/button.svelte";

  let todos = [
    { id: 1, title: "Buy milk", status: "new" },
    { id: 2, title: "Do laundry", status: "new" },
    { id: 3, title: "Make bed", status: "new" },
    { id: 4, title: "Pick up kids from school", status: "new" },
  ];

  const handleClick = () => console.log("clicked");
</script>

<ul>
  {#each todos as todo (todo.id)}
    <li class={todo.status}>{todo.title}</li>
  {/each}
</ul>
<Button onClick={handleClick}/>

<style>
  ul {
    display: flex;
    flex-direction: column;
    gap: 1em;
  }

  ul > li {
    display: block;
    border: solid;
    padding: 1rem;
    transition: .5s all ease;
  }

  ul > li:hover {
    background: var(--main-color);
    cursor: pointer;
  }

  .new {
    background: rgba(0, 255, 0, .2);
  }

  .new:hover {
    background: var(--main-color);
  }
</style>

