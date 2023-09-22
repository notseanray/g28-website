<script lang="ts">
    import { ismobile } from "../../store";
    let window: any;
</script>

<div class={"flex align-middle justify-center mx-[7vw] bg-[#d9d9d9] flex-wrap p-14 " + ($ismobile ? "rounded-[25%/8%]" : "rounded-[12%/25%]")}>
    <div class="m-5">
        <div class="flex justify-center align-middle antionio">
            <div class="text-5xl font-bold">about our team</div>
        </div>
        <div class="text-2xl">
            <div class="flex justify-center align-middle">
                <div>
                    G28 Robotics is a competitive FRC community team with members from
                    all over the Metro Atlanta area. Our mission is to bring real life
                    manufacturing and engineering exposure to students while competing
                    at a high level.
                </div>
            </div>
            <div class="flex justify-center align-middle">
                <div>
                    We are currently composed of 8 members predominantly from Wheeler
                    High School and North Cobb. By partnering with a local startup, we
                    provide a place where students foster strong passions for
                    programming, engineering, and design while honing their leadership,
                    critical thinking, and problem-solving skills.
                </div>
            </div>
        </div>
    </div>
    <div class="m-5">
        <div class="flex justify-center align-middle antionio">
            <div class="text-6xl font-bold">FIRST</div>
        </div>
        <div class="text-2xl">
            <div class="flex justify-center align-middle">
                <div
                    class="flex flex-wrap justify-center text-right float-right w-full"
                >
                    <div
                        class="text-boxes m-2 descriptions content-center text-left w-2/3 italic"
                    >
                        "FIRST creates programs where its participants are limited only
                        by the bounds of their imagination and gives them a forum to
                        begin to examine the world’s problems by exploring science,
                        technology, engineering and math."
                        <br />
                        - Congressman Jim Langevin (RI)
                        <br />
                    </div>
                    {#if !$ismobile}
                        <iframe
                            class="ml-6 rounded-md float-right"
                            width={(window ? window.innerWidth : 1000) / 3}
                            src="https://www.youtube.com/embed/Jd29kzjclV0"
                            title="YouTube video player"
                            frameborder="0"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                            allowfullscreen
                        />
                    {:else}
                        <div class="flex flex-center justify-center">
                            <iframe
                                class="ml-6 rounded-md float-right"
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
                </div>
            </div>
            FIRST stands “For Inspiration and Recognition of Science and Technology,” is
            a non-profit organization for students of STEM. The intent of FIRST is “to create
            a world where science and technology are celebrated… where young people dream
            of becoming science and technology heroes…” -Dean Kamen (Founder of FIRST).
        </div>
    </div>
    <div class="bg-[#baa4e7] max-w-[300px] w-[100%] rounded-full text-2xl visited:text-slate-50 text-slate-50 text-slate-50 text-center">
        <a href="https://www.firstinspires.org/robotics/frc"> learn more </a>
    </div>
</div>
