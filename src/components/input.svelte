<script>
  let value;
  export let name;
  export let fun;
  const handleKeyd = (e) => {
    if (e.code == "Enter") {
      e.preventDefault();
      e.target.value;
      fun(e.target.value, name);
      return false;
    } else {
      e.target.value;
      value = e.target.value;
      return false;
    }
  };
</script>

<main>
  <div><label for={value}>{name}</label></div>

  <input
    type="text"
    on:keypress={handleKeyd}
    bind:value
    name={value}
    class="input"
  />
</main>

<style>
  div {
    margin: auto;
    width: 100%;
    margin-bottom: 10px;
    max-width: 700px;
  }
  label {
    display: block;
    width: 100%;
    text-align: left;
    color: #ffffff;
  }
  input {
    margin: auto;
    margin-bottom: 20px;
    width: 700px;
    height: 40px;
    max-width: 100%;
    color: #242424;
    border-radius: 5px;
    padding: 10px 10px;
    border: none;
    font-family: "Lato", sans-serif;
    font-weight: 500;
    background: #fff;
    transition: all 0.5s ease;
    display: block;
    outline: none;
    box-shadow: 0 3px 1px -2px rgba(0, 0, 0, 0.2),
      0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12);
  }
  input::-webkit-outer-spin-button,
  input::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
  }

  /* Firefox */
  input[type="text"] {
    -moz-appearance: textfield;
  }
</style>
