<script lang="ts">
    import { ismobile } from "../../store";
</script>

<div class={"align-middle justify-center mx-[5vw] bg-[#d9d9d9] p-14 " + ($ismobile ? "rounded-[25%/23%]" : "rounded-[12%/25%]")}>
	<div class="flex justify-center mt-10">
		<div class="flex flex-wrap">
			<div class="flex flex-wrap">
				<div class="max-w-md mt-3">
					<div class="garet italic text-xl font-bold">
						G28 Robotics helps you build valuable life skills!
					</div>
					<div class="text-lg max-w-5xl">
						Please contact us here if you are interested in joining
					</div>
				</div>
			</div>
		</div>
	</div>
	<div class="flex justify-center min-w-xl">
		<div class="bg-[#baa4e7] w-8/12 rounded-full text-3xl text-[#b9b9b9] text-center">
			<a href="mailto:g28robotics@gmail.com">contact</a>
		</div>
	</div>
</div>
