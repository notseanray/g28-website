<script lang="ts">
	import "../app.css";
    import { onMount } from "svelte";
    import { Gradient } from "../Gradient";
    // Call `initGradient` with the selector to your canvas
    onMount(() => {
        const gradient = new Gradient()

        // @ts-ignore
        gradient.initGradient("#gradient")
        })
</script>
<div class="z-50 absolute text-[#ffffff]">
	<div class="raleway text-4xl m-5 flex">
		<a href="/" class="mr-12 hover:underline">
			about
		</a>
		<a href="/shop" class="mr-12 hover:underline">
			our shop
		</a>
		<a href="/sponsors" class="mr-12 hover:underline">
			sponsors
		</a>
	</div>
	<slot />
</div>
<canvas id="gradient" class="min-h-full h-full fixed">
</canvas>

<style global>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Jost&family=Raleway:wght@500&display=swap');

.raleway {
	font-family: 'Raleway', sans-serif;
}
.jost {
	font-family: 'Jost', sans-serif;
}

#gradient {
  width:100%;
  height:100%;
  --gradient-color-1: #714098;
  --gradient-color-2: #8c8ca9;
  --gradient-color-3: #363636;
  --gradient-color-4: #575b64;
}
</style>
