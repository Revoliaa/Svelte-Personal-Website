<script>
    import Home from "./components/Home.svelte";
    import Projects from "./components/Projects.svelte";
    import Contact from "./components/Contact.svelte";

    let current = "Home";

    const goToHomePage = () => {
        current = "Home";
    };

    const goToProjectsPage = () => {
        current = "Projects";
    };

    const goToContactPage = () => {
        current = "Contact";
    };
</script>

<main>
    <div class="buttons">
        <div class="btn-wrapper">
            <button class="home" on:click={goToHomePage}
                ><i class="fa-solid fa-house" /></button
            >
        </div>
        <div class="btn-wrapper">
            <button class="projects" on:click={goToProjectsPage}
                ><i class="fa-solid fa-folder" /></button
            >
        </div>
        <div class="btn-wrapper">
            <button class="contact" on:click={goToContactPage}
                ><i class="fa-solid fa-envelope" /></button
            >
        </div>
    </div>
    {#if current === "Home"}
        <Home />
    {:else if current === "Projects"}
        <Projects />
    {:else}
        <Contact />
    {/if}
</main>

<style>
    main {
        max-height: 680px;
        max-width: 960px;
        min-width: 300px;
        height: 100%;
        width: 100%;
        margin: 0px 100px;
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        border-radius: var(--radius);
        color: var(--neutral-100);
    }

    .buttons {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-end;
        gap: 20px;
        position: relative;
    }

    .btn-wrapper {
        height: 70px;
        width: 70px;
        position: relative;
    }

    button {
        aspect-ratio: 1;
        height: 70px;
        width: 80px;
        font-size: 1.5rem;
        border-radius: var(--radius) 0px 0px var(--radius);
        background-color: var(--blue);
        color: var(--neutral-100);
        position: absolute;
        top: 0;
        right: -10px;
        transition: right 0.3s;
        cursor: pointer;
    }

    button:hover {
        right: 0px;
    }

    @media screen and (max-width: 768px) {
        .btn-wrapper {
            height: 60px;
            width: 60px;
        }

        button {
            max-height: 60px;
            max-width: 70px;
            font-size: 1.25rem;
        }
    }

    @media screen and (max-width: 568px) {
        .btn-wrapper {
            height: 50px;
            width: 50px;
        }

        button {
            max-height: 50px;
            max-width: 60px;
            font-size: 1rem;
        }
    }
</style>
