<!-- <script>
    import result from './result.svelte';

    let data = [
        { id: 1, percentage: 75 },
        { id: 2, percentage: 50 },
        { id: 3, percentage: 90 },
        { id: 4, percentage: 30 },
        { id: 5, percentage: 60 },
        { id: 6, percentage: 85 }
    ];
</script>

<style>
    .dashboard {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 20px;
        padding: 20px;
    }
</style>

<div class="dashboard">
    {#each data as item (item.id)}
        <result {percentage}={item.percentage} />
    {/each}
</div> -->
<script>
    import CircularProgress from './CircularProgress.svelte';

    let data = [
        { id: 1, percentage: 75 },
        { id: 2, percentage: 50 },
        { id: 3, percentage: 90 },
        { id: 4, percentage: 30 },
        { id: 5, percentage: 60 },
        { id: 6, percentage: 85 }
    ];
</script>

<style>
    .dashboard {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 20px;
        padding: 20px;
    }
</style>

<div class="dashboard">
    {#each data as item (item.id)}
        <CircularProgress {percentage}={item.percentage} />
    {/each}
</div>
