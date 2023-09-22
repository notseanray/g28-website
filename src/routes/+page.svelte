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
    <div class="flex align-middle justify-center mx-[7vw] rounded-[12%/25%] bg-[#d9d9d9]">
        <img
            class="justify-center align-middle w-[86vw]"
            src="/g28mainpage.png"
            alt=""
        />
    </div>
{:else}
<div class="flex align-middle justify-center flex-wrap mx-[5vw]">
    <img class="w-1/3 z-50" src="/g28mill.png" alt="" />
    <img class="w-12/12 z-50" src="/g28square_nobg.png" alt="" />
</div>
{/if}
