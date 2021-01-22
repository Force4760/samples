<script>
  import Input from "./components/input.svelte";
  import Btn from "./components/btn.svelte";
  import Btn2 from "./components/btn2.svelte";
  const open = (value, name) => {
    if (name === "Tracklib Song") {
      value = value.replace(" ", "%20");
      value = `https://www.tracklib.com/tracks/?q=` + value;
    } else if (name === "Tracklib Collections") {
      value = value.replace(" ", "%20");
      value = `https://www.tracklib.com/collections/?q=` + value;
    } else if (name === "LoopCloud") {
      value = value.replace(" ", "%20");
      value =
        "https://sounds.loopcloud.com/search?q=" +
        value +
        "&partial_query=" +
        value +
        "&user=true&shop=true&wave=true&page=1";
    } else if (name === "Landr") {
      value = value.replace(" ", "%20");
      value = `https://samples.landr.com/browse?textSearch=` + value;
    } else if (name === "Sounds") {
      value = value.replace(" ", "%20");
      value = `https://sounds.com/samples/search?keyword=` + value;
    }
    var win = window.open(value, "_blank");
    win.focus();
  };
  const bt = (name) => {
    let value;
    if (name === "Splice") {
      value = "https://splice.com/sounds/catalog";
      var win = window.open(value, "_blank");
      win.focus();
    }
  };
</script>

<main>
  <h1>PAID SAMPLES</h1>
  <Input name="Tracklib Song" fun={open} />
  <Input name="Tracklib Collections" fun={open} />
  <Input name="LoopCloud" fun={open} />
  <Input name="Landr" fun={open} />
  <Btn2 text="Splice" calc={bt} />
</main>

<style>
  h1 {
    color: white;
    text-shadow: 0px 2px 5px rgba(0, 0, 0, 0.5);
  }
</style>
