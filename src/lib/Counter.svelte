<script>
  import { Sound } from "svelte-sound";
  import boom from "../assets/boom.wav";
  import chak from "../assets/chak.wav";
  import softcym from "../assets/softcymbal.wav";
  import loudcym from "../assets/loudcymbal.wav";

  const boom_sound = new Sound(boom);
  const chak_sound = new Sound(chak);
  const softcym_sound = new Sound(softcym);
  const loudcym_sound = new Sound(loudcym);

  function playChak() {
    console.log("chak")
    chak_sound.play();
  } // playSound can be called anywhere in the code

  const playBoom = () => {
    console.log("boom");
    boom_sound.play();
  }
  const playSoftCym = () => {
    console.log("soft");
    softcym_sound.play();
  }
  const playLoudCym = () => {
    console.log("loud");
    loudcym_sound.play();
  }

</script>

<main>
  <div>
    <button on:click={playLoudCym}>
      loud
    </button>
    <button on:click={playBoom}>
      boom
    </button>
    <button on:click={playBoom}>
      boom
    </button>
    <button on:click={playLoudCym}>
      loud
    </button>
  </div>
  <div>
    <button on:click={playSoftCym}>
      soft
    </button>
    <button on:click={playChak}>
      chak
    </button>
    <button on:click={playChak}>
      chak
    </button>
    <button on:click={playSoftCym}>
      soft
    </button>
  </div>
</main>