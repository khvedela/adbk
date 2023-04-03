<script>
    import { Card, Button } from "flowbite-svelte";
    let imageCount = [1,2,3,4,5,6,7,8,9];
</script>

<main>
    {#each imageCount as image}
        <img src="images/{image}.jpg" alt="love">
        <!-- <Card img="images/{image}.jpg"></Card> -->
    {/each}
</main>

<style>
    main {
        display: flex;
        gap: calc(1rem + 30px);
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: calc(100vh - 64px);
        margin-bottom: 500px;
    }

    img {
        max-height: 70vh;
        max-width: 75vw;
        border-radius: 15px;
        outline: 15px solid rgba(181, 91, 255, 0.145);
        box-sizing: border-box;
    }
</style>