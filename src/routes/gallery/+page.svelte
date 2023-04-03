<script>
    import { Card, Button } from "flowbite-svelte";
    let imageCount = [1,2,3,4,5,6,7,8,9];
</script>

<main>
    {#each imageCount as image}
        <Card img="images/{image}.jpg">
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
                20/10/2023
            </p>
        </Card>
    {/each}
</main>

<style>
    main {
        display: flex;
        gap: 1rem;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
    }
</style>