<script>
    import projects from "$lib/Projects";
</script>

<svelte:head>
    <title>Florian Didron — Experience</title>
</svelte:head>

<div class="projectContainer">
    <div class="projects">
        <h1>Experience</h1>
        {#each projects as project}
            <div class="project">
                <div class="header">
                    <h2>
                        {project.title}
                    </h2>
                    <div class="techsContainer">
                        Technologies:
                        <div class="techs">
                            {#each project.technologies as tech, idx}
                                <div>
                                    {tech}
                                    {#if idx < project.technologies.length - 1}
                                        -
                                    {/if}
                                </div>
                            {/each}
                        </div>
                    </div>
                </div>
                <p>
                    {#if project.slug == "zsa"}
                        <p>
                            A company building open-source keyboards for serious developers,
                            creative professionals, and people who care deeply about their craft.
                        </p>
                        <p>
                            Working for ZSA has been my main occupation for the past 6 years and it
                            has been a delightful experience. As the lead developer my main role
                            there is to develop the <a
                                href="https://configure.zsa.io/moonlander/layouts/default/latest/0"
                                target="_blank"
                                rel="noopener nofollow">Oryx configurator</a
                            >. Oryx is a React application communicating with a backend written in
                            Ruby on Rails using graphql as the communication protocol. You can read
                            more about the project
                            <a
                                href="https://www.zsa.io/oryx"
                                target="_blank"
                                rel="noopener nofollow">here</a
                            >.
                        </p>
                        <p>
                            It allows keyboard users to customize their layout, compile the
                            resulting firmware on our servers and flash it to their keyboard from
                            the comfort of their web browser without requiring any C knowledge.
                            Alternatively, they can also download the firmware and flash it with <a
                                href="https://www.zsa.io/wally/"
                                target="_blank"
                                rel="noopener nofollow">Wally</a
                            >, a cross platform desktop application I also developed.
                        </p>
                        <p>
                            I'm also responsible for managing the infrastructure, nothing fancy
                            here, the glorious monolith is hosted on a VM, communicating with a
                            PostgreSQL server hosted on the same sub network. Kubernetes ? No.
                        </p>
                        <p>
                            Another role is to work and contribute back to the <a
                                target="_blank"
                                rel="noopener nofollow"
                                href="https://github.com/qmk/qmk_firmware"
                            >
                                open-source firmware</a
                            > running on the keyboards.
                        </p>
                        <p>
                            Finally more recently I have been invovled in hardware design, the
                            keyboard production process and touched on the wonderful world of low
                            level coding and bootloaders.
                        </p>
                    {/if}
                    {#if project.slug == "111studio"}
                        <p>
                            I Co-Founded 111Studio K.K, a japanese software development consultancy
                            building custom software and managing teams and change for large
                            japanaese and international companies. Throughout the 7 years of
                            operating the company, I kept a developer role while managing a small
                            team of developers and designers.
                        </p>
                        <p>The company was sold to one of our clients.</p>
                    {/if}
                    {#if project.slug == "mccann"}
                        <p>A role I took as a service provider for 111Studio.</p>
                        <p>
                            Dispatched at Google Tokyo for two year on behalf of McCann Worldgroup,
                            I was responsible for the operation of Google Adsense email marketing
                            campaigns for the APAC Region.
                        </p>
                    {/if}
                    {#if project.slug == "parrot"}
                        <p>The job that bringed me to Japan !</p>
                        <p>
                            I was in charge of validating software releases for Japanese customers
                            (Bluetooth Hardware and Software package for the automotive industry).
                        </p>
                    {/if}
                    {#if project.slug == "thales"}
                        <p>
                            I was a Software Engineer working on Orange's billing software (Printing
                            and Web Portal). Responsible of software enhancement studies and
                            development.
                        </p>
                    {/if}
                    {#if project.slug == "alcatel"}
                        <p>
                            Level 2 IT Administrator for Alcatel Europe & South's datacenter
                            including system administration (HP-UX / Solaris / Suse / Windows 2003
                            Server) as well as software administration (SAP / Lotus Domino /
                            WebMethods).
                        </p>
                    {/if}
                </p>
            </div>
        {/each}
    </div>
</div>

<style>
    .projectContainer {
        width: 100%;
        max-width: 900px;
        display: flex;
        justify-content: center;
        box-sizing: border-box;
        text-align: center;
        padding: 1em;
        margin: 0 auto;
        text-align: center;
    }

    .note {
        opacity: 0.5;
        margin: 0;
        max-width: 900px;
        text-align: left;
    }

    a {
        text-decoration: none;
    }

    .projectContainer .projects {
        display: grid;
        grid-template-columns: 1fr;
        grid-gap: 40px;
        margin-top: 30px;
    }

    h1 {
        font-weight: 700;
        text-align: start;
    }

    h2 {
        display: flex;
        margin: 0;
    }

    .project {
        text-align: start;
        box-sizing: border-box;
        display: flex;
        flex-direction: column;
        color: white;
        background: #111;
        padding: 2rem;
        width: 100%;
        border-radius: 5px;
        transition: transform 0.2s ease-in-out;
        border-radius: 25px;
    }

    .project p {
        font-weight: 100;
        color: #e0e4e9;
    }

    .projects {
        width: 100%;
        margin: 50px auto;
        display: grid;
        grid-gap: 1rem;
        grid-template-columns: 1fr;
        margin-bottom: 10px;
    }

    .techsContainer {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
    }

    .techs {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .techs > div {
        margin: 0 0 0 10px;
    }

    .button {
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        border: 2px solid white;
        padding: 10px;
    }

    @media (min-width: 900px) {
        .projectContainer {
            padding: 0;
        }
        .projects > h1 {
            font-size: 48px;
            margin: 50px 0 0 0;
        }

        .projects {
            grid-template-columns: 1fr;
        }

        .projects .project {
            min-height: 200px;
        }
        .button {
            max-width: 200px;
        }
    }

    @media (min-width: 600px) {
        .projects {
            grid-template-columns: 1fr;
        }
    }
</style>
