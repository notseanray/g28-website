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
<img class="z-0 absolute -translate-x-[45vw] h-[30vw] rotate-12 w-screen" src="/blob_1.svg" alt="" />
<img class="z-0 absolute translate-x-[45vw] h-[30vw] w-screen mt-[40rem]" src="/blob_2.svg" alt="" />
<img class="z-0 absolute -translate-x-[42vw] h-[30vw] rotate-12 w-screen mt-[140vh]" src="/blob_3.svg" alt="" />
<div class="absolute flex justify-center align-middle text-center w-screen mt-[35vh] z-10">
    <div class="justify-center align-middle text-center">
        <div class="jost title">
            G-28 Robotics
        </div>
        <div class="jost frclabel float-right mr-2">
            FRC 202400169
        </div>
    </div>
</div>
<div class="mt-[100vh] w-[90vw]" />
<div class="flex flex-wrap justify-center max-w-fit mx-[3%] z-10">
    <div class="flex justify-center text-center mr-2">
        <div>
            <div class="mobile-name uppercase font-extrabold flex ml-2 z-10">
                first
                {#if !mobile}
                    <img class="ml-16 h-36 m-2 rounded-md" src="/first.png" alt="" />
                {/if}
            </div>
            <div>
                <div class="text-boxes m-2 descriptions content-center text-left mt-8">
                    The FIRST Robotics Competition is an international high-school competitive robots
                    competition centered around industry-scale robots. Each year a new challenge is
                    released on January 7, and teams have 7 weeks to design and build their robots before
                    competing with them. Our team is located in the Peachtree District (encompassing
                    Georgia and South Carolina). We will be competing in the Gwinnett and Carrollton PCH
                    District Qualifiers on 3/9-3/11 and 3/23-3/25 respectively, with the goal of advancing
                    to PCH District Champs and FIRST Champs.
                </div>
            </div>
        </div>
    </div>

    <div class="flex justify-center mt-4 text-right float-right ml-2 z-10">
        <div class="flex flex-wrap justify-center text-right float-right">
            <div class="text-boxes m-2 descriptions content-center text-right">
                "FIRST creates programs where its participants are limited only by the bounds of their
                imagination and gives them a forum to begin to examine the world’s problems by exploring
                science, technology, engineering and math.
                <br />
                - Congressman Jim Langevin (RI)
                {#if !mobile}
                    <iframe
                        class="ml-6 rounded-md float-right mt-10"
                        width="560"
                        height="315"
                        src="https://www.youtube.com/embed/Jd29kzjclV0"
                        title="YouTube video player"
                        frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen
                    />
                {:else}
                    <div class="flex flex-center justify-center">
                        <iframe
                            class="ml-6 rounded-md float-right mt-10"
                            width="250"
                            height="141"
                            src="https://www.youtube.com/embed/Jd29kzjclV0"
                            title="YouTube video player"
                            frameborder="0"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                            allowfullscreen
                        />
                    </div>
                {/if}
                <br />
            </div>
        </div>
    </div>
</div>
<div class="mt-80" />
<div class="float-right mr-[3%] mb-[20rem] z-10">
    <div class="mobile-name font-extrabold flex ml-1">the team</div>
    <div>
        <div class="text-boxes m-2 descriptions content-center text-left mt-8">
            G28-Robotics, FIRST Robotics Team 202400169, is a community-based FIRST Robotics Competition team based in Atlanta, GA. The team was founded in April of 2023 when the founders of StartProto, Tim Felbinger and Zach Cloud, offered to host a rookie team that was at risk of dissolving at StartProto HQ.
<br />
<br />
The team has a focus on giving students unique, real-world experience with both engineering and manufacturing. Some of our students spent the summer working at manufacturers and software companies. We are planning on competing in the 2024 FIRST Robotics Competition.
<br />
<br />
Want to support our mission? Here’s how you can get involved:
<br />
<br />
Join our Team: <a href="/join" class="hover:underline">Mentors / Students</a>
<br />
<a href="/sponsors" class="hover:underline">Become a Sponsor</a>


        </div>
    </div>
    <div class="flex mt-8">
        <div class="flex flex-wrap max-w-full team-profile">
            <!-- <img class="mx-4 my-4 h-60 rounded-md" src={ian_oberbeck} alt="" /> -->
            <!-- <img class="mx-4 my-4 h-60 rounded-md" src={jacob_dymkowski} alt="" /> -->
            <!-- <img class="mx-4 my-4 h-60 rounded-md" src={leona_longhurst} alt="" /> -->
            <!-- <img class="mx-4 my-4 h-60 rounded-md" src={sameeh_pottayil} alt="" /> -->
            <!-- <img class="mx-4 my-4 h-60 rounded-md" src={sean_ray} alt="" /> -->
        </div>
    </div>
</div>
<style>
</style>
