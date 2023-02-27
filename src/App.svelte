<script lang="ts">
  let firstName = "Estifanos";
  let lastName = "Beyene";
  let color = "blue";
  let showText = false;
  let users = [
    {
      id: "1",
      name: "John",
    },
    {
      id: "2",
      name: "Abel",
    },
    {
      id: "3",
      name: "Jake",
    },
  ];

  $: name = firstName + " " + lastName;

  const toggle = () => {
    color === "blue" ? (color = "purple") : (color = "blue");
    showText = !showText;
    users = [...users, { id: `${users.length + 1}`, name: `new` }];
  };
</script>

<main>
  <h1 style="color: {color}">{name}</h1>
  <button on:click={toggle}>Click</button>
  {#if showText}
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi dolorum
      molestiae rem optio reiciendis. Vero saepe porro aperiam impedit
      distinctio, qui repellendus excepturi, quo provident alias nostrum?
      Cupiditate, voluptatem id.
    </p>
  {:else}
    <p>No Paragraph</p>
  {/if}

  <ul>
    {#each users as user}
      <li>{user.id}: {user.name}</li>
    {/each}
  </ul>
</main>
