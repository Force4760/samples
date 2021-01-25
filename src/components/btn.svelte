<script>
  export let calc;
  export let text;
</script>

<main>
  <button on:click={() => calc(text)} class="btn"><span>{text}</span></button>
</main>

<style>
  .btn {
    margin-bottom: 20px;
    margin-left: 16px;
    margin-right: 16px;
    width: 210px;
    height: 50px;
    color: #fff;
    border-radius: 5px;
    padding: 10px 25px;
    border: none;
    font-family: "Lato", sans-serif;
    font-weight: 500;
    background: #166b57;
    cursor: pointer;
    transition: all 0.5s ease;
    position: relative;
    display: inline-block;
    outline: none;
    box-shadow: 0 3px 1px -2px rgba(0, 0, 0, 0.2),
      0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12);
  }

  .btn:hover {
    background: #115041;
    box-shadow: 0 2px 4px -1px rgba(0, 0, 0, 0.2),
      0 4px 5px 0 rgba(0, 0, 0, 0.14), 0 1px 10px 0 rgba(0, 0, 0, 0.12);
  }
</style>
