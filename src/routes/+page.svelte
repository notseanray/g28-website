<script lang="ts">
    import { ismobile } from '../store';

    import { browser } from '$app/environment';
    let mobile: boolean;
	if (browser) {
		ismobile.subscribe((d) => {
			mobile = d;
		});
	}
</script>
<div class="flex align-middle justify-center">
    <img class="justify-center align-middle w-[50vw]" src="/g28background.png" alt="" />
</div>
