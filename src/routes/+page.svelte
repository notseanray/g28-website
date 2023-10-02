<script lang="ts">
    import { ismobile } from "../store";

    import { browser } from "$app/environment";
    let mobile: boolean;
    if (browser) {
        ismobile.subscribe((d) => {
            mobile = d;
        });
    }
</script>

{#if !mobile}
    <div class="flex align-middle justify-center mx-[5vw]">
        <img class="max-w-1/3 w-[10vw] z-50" src="/g28mill.png" alt="" />
        <img class="max-w-6/12 w-[30vw] z-50" src="/g28square_nobg.png" alt="" />
    </div>
{:else}
<div class="flex align-middle justify-center flex-wrap mx-[5vw]">
    <img class="w-1/3 z-50" src="/g28mill.png" alt="" />
    <img class="w-12/12 z-50" src="/g28square_nobg.png" alt="" />
</div>
{/if}
<div class="flex align-middle justify-center flex-wrap mx-[5vw] antionio text-5xl">
    FRC 9500
</div>
