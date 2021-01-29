<script>
  import Input from "./components/input.svelte";
  import Btn from "./components/btn.svelte";
  import Btn2 from "./components/btn2.svelte";
  import Select from "./components/select.svelte";
  let sOrSP = "Samples";
  const bt = (name) => {
    let value;
    if (name === "Vinyl Frontier Plus") {
      value = "https://www.youtube.com/channel/UC8sdN6rOzGrCHDIDHTK_2KA";
    } else if (name === "Andre navarro II") {
      value = "https://www.youtube.com/channel/UCv5OAW45h67CJEY6kJLyisg";
    } else if (name === "Vinyl Frontier East II") {
      value = "https://www.youtube.com/channel/UCKMcwyZqQO3jcEF1BymFDMw";
    } else if (name === "Το φιλί της Πεταλούδας") {
      value = "https://www.youtube.com/channel/UCTdk8oVdKsn4bfq64O4A6HA";
    } else if (name === "Foreal1992") {
      value = "https://www.youtube.com/user/foreal1992";
    } else if (name === "Pedro Nóbrega") {
      value = "https://www.youtube.com/user/Verseucht";
    } else if (name === "Ricardo Maraña") {
      value = "https://www.youtube.com/c/RicardoMara%C3%B1a/featured";
    } else if (name === "Sonne Immage") {
      value = "https://www.youtube.com/user/sonneimmage";
    } else if (name === "Soulhawk") {
      value = "https://www.youtube.com/user/TheSoulhawk";
    } else if (name === "Aquarianrealm") {
      value = "https://www.youtube.com/c/aquarianrealm/videos";
    } else if (name === "MiamiBornAgain") {
      value = "https://www.youtube.com/user/MiamiBornAgain";
    } else if (name === "Yousoulme Cbwasa") {
      value = "https://www.youtube.com/channel/UCdr1C2pntbnNP3QpYDp14sA";
    } else if (name === "My Analog Journal") {
      value = "https://www.youtube.com/user/zagorofficial";
    } else if (name === "VIVAVINYL") {
      value = "https://www.youtube.com/channel/UCHR68qYjV2yJ87azCO7bwIQ";
    } else if (name === "Brazilian Rare Grooves") {
      value = "https://www.youtube.com/channel/UC8ya7uaEIuwo3lRn54gpRZw";
    } else if (name === "2chann") {
      value = "https://www.youtube.com/user/TVchannel02";
    } else if (name === "XTNDO P") {
      value = "https://www.youtube.com/channel/UCE8iI7HWw1dJacD0wZcgu5g";
    } else if (name === "Producer Dojo") {
      value = "https://www.youtube.com/user/ryandiedx";
    } else if (name === "BUYLOOPS") {
      value = "https://www.youtube.com/c/BUYLOOPS/featured";
    } else if (name === "Chubby Beatz") {
      value = "https://www.youtube.com/channel/UCHPgK7BemhM0e18mWiPmYpg";
    } else if (name === "April 4th") {
      value = "https://www.youtube.com/channel/UCqRl57uODIR4hO26XxOE1_w";
    } else if (name === "Enlies Beats") {
      value = "https://www.youtube.com/channel/UCV8FFSKsCrNSu-ZzWs2DQfA";
    } else if (name === "sxber") {
      value = "https://www.youtube.com/channel/UCidLsKl1PiHHb5rjXx5nh6A";
    } else if (name === "EOS Sample Pack") {
      value = "https://www.youtube.com/channel/UCuFNNNMpHDS3jpKeH5uixjg";
    } else if (name === "En-Beat Tube") {
      value = "https://www.youtube.com/channel/UCEPUhsYA_z7B5r1bOWHFeRw";
    } else if (name === "Sample Machine") {
      value = "https://www.youtube.com/channel/UCO20872j2XmOfZ4s3A4q1AQ";
    } else if (name === "AYPE") {
      value = "https://www.youtube.com/channel/UCiQx1K5mJQZIHufeCn0KpvQ";
    } else if (name === "CO KAYN") {
      value = "https://www.youtube.com/channel/UCDnWxJUmx5RWfBlfS1tN48g";
    } else if (name === "Dave Zeke Jr.") {
      value = "https://www.youtube.com/channel/UCrwFtp-FM7UKvc4Un_kcDtw";
    } else if (name === "THE KIT PLUG") {
      value = "https://www.youtube.com/channel/UCf9rcjI6BJOWWNelpWEXIxg";
    } else if (name === "Gousty Loops") {
      value = "https://www.youtube.com/channel/UCUt0m_5GqS1rN_2NhOCstrQ";
    }

    var win = window.open(value, "_blank");
    win.focus();
  };
</script>

<main>
  <h1>YOUTUBE SAMPLES</h1>
  <Select name="" ops={["Samples", "Samples Packs"]} bind:value={sOrSP} />
  {#if sOrSP === "Samples"}
    <Btn2 text="Vinyl Frontier Plus" calc={bt} />
    <Btn2 text="Vinyl Frontier East II" calc={bt} />
    <Btn2 text="Το φιλί της Πεταλούδας" calc={bt} />
    <Btn2 text="Andre navarro II" calc={bt} />
    <Btn2 text="Foreal1992" calc={bt} />
    <Btn2 text="Pedro Nóbrega" calc={bt} />
    <Btn2 text="Ricardo Maraña" calc={bt} />
    <Btn2 text="Sonne Immage" calc={bt} />
    <Btn2 text="Soulhawk" calc={bt} />
    <Btn2 text="Aquarianrealm" calc={bt} />
    <Btn2 text="MiamiBornAgain" calc={bt} />
    <Btn2 text="Yousoulme Cbwasa" calc={bt} />
    <Btn2 text="My Analog Journal" calc={bt} />
    <Btn2 text="VIVAVINYL" calc={bt} />
    <Btn2 text="Brazilian Rare Grooves" calc={bt} />
    <Btn2 text="2chann" calc={bt} />
  {:else}
    <Btn2 text="XTNDO P" calc={bt} />
    <Btn2 text="Producer Dojo" calc={bt} />
    <Btn2 text="BUYLOOPS" calc={bt} />
    <Btn2 text="April 4th" calc={bt} />
    <Btn2 text="Chubby Beatz" calc={bt} />
    <Btn2 text="Enlies Beats" calc={bt} />
    <Btn2 text="sxber" calc={bt} />
    <Btn2 text="EOS Sample Pack" calc={bt} />
    <Btn2 text="En-Beat Tube" calc={bt} />
    <Btn2 text="Sample Machine" calc={bt} />
    <Btn2 text="AYPE" calc={bt} />
    <Btn2 text="CO KAYN" calc={bt} />
    <Btn2 text="Dave Zeke Jr." calc={bt} />
    <Btn2 text="THE KIT PLUG" calc={bt} />
    <Btn2 text="Gousty Loops" calc={bt} />
  {/if}
</main>

<style>
  h1 {
    color: white;
    text-shadow: 0px 2px 5px rgba(0, 0, 0, 0.5);
  }
</style>
