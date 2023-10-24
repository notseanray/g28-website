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

<div class="flex align-middle justify-center flex-wrap mx-[5vw]">
    <img class="w-1/3 z-50" src="/logo.png" alt="" />
</div>
<div class="flex align-middle justify-center flex-wrap mx-[5vw] antionio text-5xl">
    FRC 9500
</div>
