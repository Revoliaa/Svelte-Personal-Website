<script>
    const skills = [
        {
            id: 1,
            name: "Html",
            img: "./images/html.svg",
            value: "90%",
        },
        {
            id: 2,
            name: "Css",
            img: "./images/css.svg",
            value: "75%",
        },
        {
            id: 3,
            name: "Javascript",
            img: "./images/js.svg",
            value: "60%",
        },
        {
            id: 4,
            name: "Svelte",
            img: "./images/svelte.svg",
            value: "20%",
        },
    ];
</script>

<section>
    <div class="intro">
        <img src="./images/profile.png" alt="Profile" />
        <p>
            Hello I'm Revolia. I am 15 years old Front End developer living in
            Turkey. I have been programming since 2021. My programming story
            started with coding Discord bot with Discord.js library then I
            interested in Front End development. Since then I have been working
            on Front End technologies. Below are some languages and frameworks
            that I using in my projects.
        </p>
    </div>
    <div class="skills">
        {#each skills as skill (skill.id)}
            <div>
                <div class="skillTitle">
                    <img src={skill.img} alt={skill.name} />
                    <p>{skill.name}</p>
                    <p class="skillInfo">{skill.value}</p>
                </div>
                <div class="skillPercentage">
                    <div style="width: {skill.value};" />
                </div>
            </div>
        {/each}
    </div>
</section>

<style>
    section {
        user-select: none;
    }

    .intro {
        margin-top: 40px;
        display: flex;
        align-items: center;
        gap: 40px;
    }

    .intro > p {
        text-indent: 30px;
    }

    .intro > img {
        max-width: 220px;
        height: auto;
        width: 100%;
        border-radius: var(--radius);
    }

    .skills {
        margin-top: 80px;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-columns: minmax(100px, auto);
        align-items: center;
        justify-items: center;
        font-size: 1.25rem;
        gap: 40px;
    }

    .skillTitle {
        display: flex;
        align-items: center;
        gap: 10px;
        margin-bottom: 10px;
        position: relative;
    }

    .skillTitle > img {
        width: 32px;
    }

    .skillInfo {
        position: absolute;
        right: 10px;
        font-size: 1rem;
        opacity: 0.6;
    }

    .skillPercentage {
        height: 8px;
        width: 300px;
        border-radius: var(--radius);
        background-color: var(--lighter);
    }

    .skillPercentage > div {
        height: 100%;
        border-radius: var(--radius);
        background-color: var(--blue);
    }

    @media (max-width: 960px) {
        .intro {
            flex-direction: column;
        }

        .skills {
            grid-template-columns: 1fr;
        }

        p {
            font-size: 1rem;
        }
    }

    @media (max-width: 600px) {
        .skillPercentage {
            width: 210px;
        }
    }
</style>
