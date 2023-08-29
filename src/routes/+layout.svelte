<script lang="ts">
	import "../app.css";
    import { onMount } from "svelte";
    import { Gradient } from "../Gradient";
    // Call `initGradient` with the selector to your canvas
    import { ismobile } from "../store";
    import { browser } from '$app/environment';
    let mobile = false;
    import { page } from '$app/stores';
    const MOBILE_WIDTH = 800;
    const handleResize = (e: any) => {
		mobile = window.innerWidth < MOBILE_WIDTH;
        ismobile.set(mobile);
	};
	if (browser) {
		handleResize(undefined);
		const debounce = (fn: (e: any) => void, interval: number) => {
			let timer: any;
			return function debounced(...args: any) {
				clearTimeout(timer);
				timer = setTimeout(function call() {
					fn(args);
				}, interval);
			};
		};
		window.addEventListener('resize', debounce(handleResize, 2));
	}
    onMount(() => {
        const gradient = new Gradient()

        // @ts-ignore
        gradient.initGradient("#gradient")
	});
</script>
<div class="w-screen overflow-hidden">
<div class="w-full z-50 absolute text-[#ffffff] overflow-hidden">
    <div class="raleway navtext m-2 flex h-40 justify-self-end tracking-tight">
        {#if !mobile}
            <a href="/">
                <img class="h-20" src="/logo.png" alt="" />
            </a>
        {/if}
        <div class="ht-20 p-5">
            {#if $page.url.pathname === '/' ? 'page' : undefined}
                <a href="/" class="text-slate-[#D7D6D6] mr-4">
                    about
                </a>
            {:else}
                <a href="/" class="text-slate-100 mr-4">
                    about
                </a>
            {/if}
            {#if $page.url.pathname === '/join' ? 'page' : undefined}
                <a href="/join" class="text-slate-[#D7D6D6] mr-4">
                    join
                </a>
            {:else}
                <a href="/join" class="text-slate-100 mr-4">
                    join
                </a>
            {/if}
            {#if $page.url.pathname === '/shop' ? 'page' : undefined}
                <a href="/shop" class="text-slate-[#D7D6D6] mr-4">
                    our shop
                </a>
            {:else}
                <a href="/shop" class="text-slate-100 mr-4">
                    our shop
                </a>
            {/if}
            {#if $page.url.pathname === '/sponsors' ? 'page' : undefined}
                <a href="/sponsors" class="text-slate-[#D7D6D6] mr-4">
                    sponsors
                </a>
            {:else}
                <a href="/sponsors" class="text-slate-100 mr-4">
                    sponsors
                </a>
            {/if}
        </div>
    </div>
    <slot />
</div>
</div>
<canvas id="gradient" class="w-[100vw] h-[100vh] fixed overflow-hidden">
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

.navtext {
    font-size: 2.25rem;
    line-height: 2.5rem;
}

#gradient {
  width:100%;
  height:100%;
  --gradient-color-1: #714098;
  --gradient-color-2: #8c8ca9;
  --gradient-color-3: #363636;
  --gradient-color-4: #575b64;
}

@media (max-width: 800px) {
    .navtext {
        font-size: 1.2rem;
        line-height: 1rem;
    }
}
</style>
