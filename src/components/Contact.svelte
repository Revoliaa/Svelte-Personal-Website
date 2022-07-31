<section>
    <div class="left">
        <form
            action="https://formspree.io/f/xknewjne"
            method="POST"
            autocomplete="off"
        >
            <p>Message Me</p>
            <input type="text" placeholder="Name" name="name" required />
            <input type="email" placeholder="E-mail" name="e-mail" required />
            <input type="text" placeholder="Subject" name="subject" required />
            <textarea
                placeholder="Message"
                cols="30"
                rows="10"
                name="message"
                required
            />
            <button type="submit" class="submitBtn">Send</button>
        </form>
    </div>
    <div class="right">
        <p>Accounts</p>

        <div class="accounts">
            <a
                href="https://github.com/Revoliaa"
                rel="nofollow noopener"
                target="_blank"><i class="fa-brands fa-github" /></a
            >
            <a
                href="https://steamcommunity.com/id/revolia"
                rel="nofollow noopener"
                target="_blank"><i class="fa-brands fa-steam" /></a
            >
            <a
                href="https://discord.com/users/546190684097347586"
                rel="nofollow noopener"
                target="_blank"><i class="fa-brands fa-discord" /></a
            >
            <a
                href="https://www.youtube.com/channel/UCriGgqSeFK7UbvAV04WXaVw"
                rel="nofollow noopener"
                target="_blank"><i class="fa-brands fa-youtube" /></a
            >
            <a
                href="https://www.twitch.tv/rev0lia"
                target="_blank"
                rel="nofollow noopener"><i class="fa-brands fa-twitch" /></a
            >
            <a
                href="https://open.spotify.com/user/uict8eznusqtlxfafq8miyvb4"
                rel="nofollow noopener"
                target="_blank"><i class="fa-brands fa-spotify" /></a
            >
            <a
                href="https://twitter.com/Rev0lia"
                target="_blank"
                rel="nofollow noopener"><i class="fa-brands fa-twitter" /></a
            >
            <a
                href="https://www.reddit.com/user/Rev0lia"
                target="_blank"
                rel="nofollow noopener"><i class="fa-brands fa-reddit" /></a
            >
        </div>
    </div>
</section>

<style>
    section {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
    }

    form {
        height: 100%;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 40px;
    }

    form > p {
        font-size: 1.5rem;
        user-select: none;
    }

    input {
        max-height: 50px;
        max-width: 360px;
        min-width: 170px;
        height: 100%;
        width: 100%;
        padding: 10px 20px;
        font-size: 1.15rem;
        background-color: var(--lighter);
        border-radius: var(--radius);
        color: var(--neutral-100);
    }

    textarea {
        max-height: 120px;
        max-width: 360px;
        min-width: 170px;
        height: 100%;
        width: 100%;
        padding: 10px 20px;
        font-size: 1.15rem;
        resize: none;
        background-color: var(--lighter);
        border-radius: var(--radius);
        color: var(--neutral-100);
    }

    .submitBtn {
        height: 50px;
        width: 150px;
        background-color: var(--lighter);
        border-radius: var(--radius);
        font-size: 1.25rem;
        color: var(--neutral-100);
        cursor: pointer;
    }

    .right {
        padding-left: 20px;
        height: 100%;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 40px;
    }

    .right > p {
        margin-top: 40px;
        font-size: 1.5rem;
        user-select: none;
    }

    .accounts {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 40px;
    }

    .accounts i {
        color: var(--blue);
        font-size: 2rem;
        transition: transform 0.6s;
    }

    .accounts i:hover {
        transform: rotateZ(360deg);
    }

    @media screen and (max-width: 960px) {
        section {
            grid-template-columns: 1fr;
        }

        .right {
            padding-left: 0px;
        }

        .accounts {
            gap: 20px;
        }
    }
</style>
