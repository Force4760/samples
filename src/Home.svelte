<script>
  import Input from "./components/input.svelte";
  import Btn from "./components/btn.svelte";
  import wordList from "random-words";

  const open = (value, name) => {
    if (name === "Youtube") {
      value = value.replace(" ", "+");
      value = `https://www.youtube.com/results?search_query=` + value;
    } else if (name === "TuneBat") {
      value = value.replace(" ", "+");
      value = `https://tunebat.com/Search?q=` + value;
    } else if (name === "Spotify") {
      value = value.replace(" ", "%20");
      value = `https://open.spotify.com/search/` + value;
    } else if (name === "Looperman") {
      value = value.replace(" ", "%20");
      value =
        `https://www.looperman.com/loops?page=1&keys=` +
        value +
        `&order=date&dir=d`;
    } else if (name === "Discogs") {
      value = value.replace(" ", "+");
      value = `https://www.discogs.com/search/?q=` + value + `&type=all`;
    } else if (name === "Who Sampled") {
      value = value.replace(" ", "+");
      value = `https://www.whosampled.com/search/?q=` + value;
    }
    var win = window.open(value, "_blank");
    win.focus();
  };
  const bt = (name) => {
    let value;
    if (name === "Radiooo") {
      value = "https://radiooooo.com/";
    } else if (name === "Radio Garden") {
      value = "http://radio.garden/";
    } else if (name === "Citizen Dj") {
      value = "https://citizen-dj.labs.loc.gov/";
    } else if (name === "Splitter") {
      value = "https://vocalremover.org/";
    } else if (name === "Drum Kits") {
      value = `https://www.reddit.com/r/Drumkits/`;
    } else if (name === "Ontiva") {
      value = `https://ontiva.com/en`;
    } else if (name === "Youtube Samples") {
      value = `#/yt`;
    } else if (name === "Paid Samples") {
      value = `#/paid`;
    } else if (name === "Random Samples") {
      let keyword = wordList(1);
      value = `https://open.spotify.com/search/` + keyword;
    }
    var win = window.open(value, "_blank");
    win.focus();
  };
</script>

<main>
  <h1>SAMPLES</h1>
  <p>
    A place for sample heads. <br /> A collection of apps and resources for
    sample based musicians. <br /> Have fun and make awesome music!
  </p>
  <Input name="Youtube" fun={open} />
  <Input name="Spotify" fun={open} />
  <Input name="TuneBat" fun={open} />
  <Input name="Discogs" fun={open} />
  <Input name="Who Sampled" fun={open} />
  <Input name="Looperman" fun={open} />

  <div class="btn">
    <Btn text="Radiooo" calc={bt} />
    <Btn text="Radio Garden" calc={bt} />
    <Btn text="Citizen Dj" calc={bt} />
    <Btn text="Splitter" calc={bt} />
    <Btn text="Drum Kits" calc={bt} />
    <Btn text="Ontiva" calc={bt} />
    <Btn text="Paid Samples" calc={bt} />
    <Btn text="Youtube Samples" calc={bt} />
    <Btn text="Random Samples" calc={bt} />
  </div>
</main>

<style>
  p {
    color: white;
    text-shadow: 0px 2px 2px rgba(0, 0, 0, 0.5);
  }
  h1 {
    color: white;
    text-shadow: 0px 2px 5px rgba(0, 0, 0, 0.5);
  }
  .btn {
    display: flex;
    flex-wrap: wrap;
    margin: auto;
    width: 90%;
    max-width: 800px;
    align-items: center;
    justify-content: center;
  }
</style>
