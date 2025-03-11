<script lang="ts">
    export let title:string;
    export let skills:string;
</script>

<div class="project">
    <h3>{title}</h3>
    <p>{skills}</p>
</div>

<style lang="scss">
    .project {
        padding: 1.5rem;
        display: flex;
        flex-direction: column;
        gap: 1rem;
        border: .5px solid $light-grey;
        border-radius: 2rem;
        color: $light-grey;
        font-family: "Fira Code";

        h3 {
            font-size: 1.5rem;
            font-weight: 400;
        }

        p {
            line-height: 2rem;
        }
    }
</style>