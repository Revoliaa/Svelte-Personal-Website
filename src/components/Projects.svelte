<script>
    const projects = [
        {
            id: 1,
            name: "Guess The Flag",
            desc: "Flag guessing game.",
            repo: "https://github.com/Revoliaa/Guess-The-Flag",
            live: "https://guess-the-flag.ml",
        },
        {
            id: 2,
            name: "Revolia.tk",
            desc: "My personal website.",
            repo: "https://github.com/Revoliaa/Revolia.tk",
            live: "https://revolia.tk",
        },
        {
            id: 3,
            name: "Batiyormuyuz.tk",
            desc: "Simple TRY based currency website.",
            repo: "https://github.com/Revoliaa/Batiyormuyuz.tk",
            live: null,
        },
        {
            id: 4,
            name: "Revo-Haste",
            desc: "Fast and simple text sharing website.",
            repo: "https://github.com/Revoliaa/Revo-Haste",
            live: null,
        },
        {
            id: 5,
            name: "Rowexa Launcher",
            desc: "Lightweight and simple Minecraft launcher.",
            repo: "https://github.com/Revoliaa/RowexaLauncher",
            live: null,
        },
        {
            id: 6,
            name: "Veison",
            desc: "Multi functional Discord bot.",
            repo: "https://github.com/Revoliaa/VeisonBOT",
            live: null,
        },
        {
            id: 7,
            name: "Svelte Personal Website",
            desc: "Personal website coded with Svelte framework",
        },
    ];
</script>

<section>
    <p class="title">Projects</p>
    <div class="projects">
        {#each projects as project (project.id)}
            <div>
                <h3>{project.name}</h3>
                <p>{project.desc}</p>
                <div class="links">
                    {#if project.repo}
                        <p>
                            <a href={project.repo} rel="nofollow noopener"
                                >GitHub</a
                            >
                        </p>
                    {/if}
                    {#if project.live}
                        <p>
                            <a href={project.live} rel="nofollow noopener"
                                >Live</a
                            >
                        </p>
                    {/if}
                </div>
            </div>
        {/each}
    </div>
</section>

<style>
    section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        gap: 40px;
    }

    .title {
        margin-top: 40px;
        font-size: 1.5rem;
        user-select: none;
    }

    .projects {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 30px;
    }

    .projects > div {
        min-height: 180px;
        height: 100%;
        width: 400px;
        background-color: var(--lighter);
        border-radius: var(--radius);
        display: grid;
        grid-auto-rows: minmax(50px, auto);
        padding: 20px;
    }

    .projects > div h3 {
        font-size: 1.5rem;
    }

    .projects > div > div {
        display: flex;
        align-items: center;
        justify-content: flex-start;
        gap: 20px;
    }

    .projects a {
        color: var(--blue);
    }

    .links {
        align-self: flex-end;
    }

    @media screen and (max-width: 1160px) {
        .projects {
            grid-template-columns: 1fr;
        }
    }

    @media screen and (max-width: 768px) {
        .projects > div {
            width: 280px;
        }
    }

    @media screen and (max-width: 568px) {
        .projects > div {
            width: 220px;
        }

        .projects > div h3 {
            font-size: 1.25rem;
        }

        .projects > div > div {
            justify-content: space-around;
        }
    }
</style>
