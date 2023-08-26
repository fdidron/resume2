<script>
    import skills from "$lib/Skills";
</script>

<svelte:head>
    <title>Florian Didron — About</title>
</svelte:head>

<div class="container">
    <main>
        <h1>About</h1>
        <p>Hi, my name is Florian, a software developer living between Japan and Thailand.</p>
        <p>
            Throughout my career, I have developed web services, desktop applications and worked on
            embeddded devices.
        </p>
        <p>
            I also have experience in managing small teams of developers and designers as I founded
            and managed a small software development company in Japan for 7 years, which I sold in
            2017.
        </p>
        <p>
            For the past 6 years, I have been working fully remote as a freelancer for various
            clients in the field of IOT, E-Commerce and Hardware development.
        </p>
        <p>
            On a more personal note, I'm a 42yo French citizen living between Bangkok and Tokyo
            since 2008, married to a Japanese national and proud father of a 9 year old daughter. I
            can speak French (Native), English (Fluent) and Japanese (Conversational). I love
            running, drumming and programming.
        </p>
        <p>You can read more about my <a href="/experience">past experience here</a>.</p>
        <h2>Skills</h2>
        {#each Object.entries(skills) as [section, technologies]}
            <ul>
                <li>
                    <h4>
                        {section}:
                    </h4>
                    <div class="list">
                        {#each technologies as technology}
                            <div>
                                {technology}
                            </div>
                        {/each}
                    </div>
                </li>
            </ul>
        {/each}
    </main>
</div>

<style>
    .container {
        max-width: 900px;
        padding: 0;
        display: flex;
        justify-content: center;
    }

    main {
        max-width: 100%;
        min-height: 500px;
        text-align: left;
        margin: 0 auto;
        box-sizing: border-box;
    }

    h1 {
        font-weight: 700;
        margin: 0 0 50px 0;
        font-size: 36px;
        text-align: start;
    }

    h2 {
        margin-top: 50px;
    }

    .list {
        display: flex;
        flex-direction: column;
        gap: 30px;
    }

    @media (min-width: 900px) {
        .list {
            flex-direction: row;
        }
        main > h1 {
            font-size: 48px;
        }
    }
</style>
