<script lang="ts">
    import "../app.css";
    // Call `initGradient` with the selector to your canvas
    import { ismobile } from "../store";
    import { browser } from "$app/environment";
    let mobile = false;
    import { page } from "$app/stores";
    const MOBILE_WIDTH = 800;
    const handleResize = (e: any) => {
        if (window) {
            mobile = window.innerWidth < MOBILE_WIDTH;
            ismobile.set(mobile);
        }
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
        window.addEventListener("resize", debounce(handleResize, 2));
    }
    /*
    onMount(() => {
        const gradient = new Gradient()

        // @ts-ignore
        gradient.initGradient("#gradient")
	});
    */
</script>

<div class="w-screen overflow-hidden">
    <div class="w-full z-50 absolute overflow-hidden">
        <div
            class="navtext m-2 flex h-40 justify-self-end tracking-tight garet z-50"
        >
            {#if !mobile}
                <a href="/">
                    <img class="w-16 z-50" src="/g28mill.png" alt="" />
                    <img class="w-16 z-50" src="/logo_vertical.png" alt="" />
                </a>
            {/if}
            <div class="ht-20 p-5 ml-5">
                <a
                    href="/"
                    class={$page.url.pathname === "/"
                        ? "text-slate-500 mr-4"
                        : "text-black mr-4"}
                >
                    home
                </a>
                <a
                    href="/about"
                    class={$page.url.pathname === "/about"
                        ? "text-slate-500 mr-4"
                        : "text-black mr-4"}
                >
                    about
                </a>
                <a
                    href="/connect"
                    class={$page.url.pathname === "/connect"
                        ? "text-slate-500 mr-4"
                        : "text-black mr-4"}
                >
                    connect
                </a>
                <a
                    href="/sponsors"
                    class={$page.url.pathname === "/sponsors"
                        ? "text-slate-500 mr-4"
                        : "text-black mr-4"}
                >
                    sponsors
                </a>
            </div>
        </div>
        <div class="flex align-middle justify-center mx-[7vw] mb-10">
            <div class="max-w-[1500px] w-[80%] min-w-[200px]">
                <slot />
            </div>
        </div>
    </div>
</div>

<!-- <div class="w-[100vw] h-[100vh] fixed z-10"> -->
<!-- <div class="w-[90vw] h-[90vh] mx-[5vw] my-[5vh] fixed opacity-15 z-20 rounded-lg overflow-hidden" /> -->
<!--     <canvas id="gradient" class="w-[90vw] h-[90vh] mx-[5vw] my-[10vh] fixed overflow-hidden rounded-[10%/20%]"> -->
<!--     </canvas> -->
<!-- </div> -->

<style global>
    @import url("https://fonts.cdnfonts.com/css/garet");
    @import url("https://fonts.googleapis.com/css2?family=Antonio&display=swap");

    .garet {
        font-family: "Garet", sans-serif;
    }
    .antionio {
        font-family: "Antonio", sans-serif;
    }

    #gradient {
        width: 90%;
        height: 80%;
        opacity: 70%;
        --gradient-color-1: #714098;
        --gradient-color-2: #8c8ca9;
        --gradient-color-3: #363636;
        --gradient-color-4: #575b64;
    }

    .navtext {
        font-size: 2.25rem;
        line-height: 2.5rem;
    }

    @media (max-width: 800px) {
        .navtext {
            font-size: 1.5rem;
            line-height: 1rem;
        }
    }
</style>
