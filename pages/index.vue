<script setup>
import socials from "assets/socials.json";
import projects from "assets/projects.json";
</script>

<template>
    <div>
        <h1 class="hi">Hi! I'm Harper.</h1>

        <div>
            <h2>A History of Ideas!</h2>
            <p>
                I'm a web developer who's always had a thing for tech, and more
                specifically creating things both for and with it.
            </p>
            <p>
                I like to branch out from web development occasionally, though. Some may
                even say I like to cause trouble. Mischeif, even.
            </p>
        </div>

        <div>
            <h2>My Lovely Projects</h2>
            <div v-for="project in projects">
                <ProjectCard :emoji="project.emoji" :color="project.color" :text="project.text" :lang="project.lang"
                    :tools="project.tools" :description="project.description" :url="project.url" />
            </div>
        </div>

        <div>
            <h2>Socials</h2>
            <div v-for="social in socials">
                {{ social.text }}
            </div>
        </div>
    </div>
</template>

<style>
body {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
        Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
</style>
