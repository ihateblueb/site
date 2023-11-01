<script>
export default {
  props: {
    emoji: String,
    color: String,
    text: String,
    lang: String,
    tools: String,
    description: String,
    url: String
  }
}
</script>

<template>
    <div class="projectCard">
        <div class="title">
            {{ text }}
        </div>
        <div class="body">
            <div class="tags">
            <div class="lang">
                {{ lang }}
            </div>
            <div class="other">
                {{ tools }}
            </div>
        </div>
        <div>
            {{ description }}
        </div>
        </div>
    </div>
</template>

<style>
.projectCard {
    display: block;
    background-color: var(--bg3);

    max-width: 350px;
    margin: 10px;
    border-radius: 10px;

    box-shadow: 0px 0px 5px var(--border);
    transition: .2s;

    border: 1px solid var(--border);

    &:hover {
        box-shadow: 0px 0px 10px var(--border);
    }

    > .title {
        font-weight: 600;
        padding: 8px 12px;
        border-bottom: 1px solid var(--border);
    }

    > .body {
        padding: 8px 12px;

        > .tags {
            margin-bottom: 8px;
        }
    }
}
</style>