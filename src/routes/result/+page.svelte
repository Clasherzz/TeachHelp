<!-- <script>
    export let percentage = 0;
</script>

<style>
    .circle {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        background: conic-gradient(
            #4caf50 calc(var(--percentage) * 1%),
            #ccc 0
        );
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 24px;
        color: #4caf50;
        position: relative;
        margin: 10px;
    }

    .circle::before {
        content: "";
        position: absolute;
        top: 10px;
        left: 10px;
        right: 10px;
        bottom: 10px;
        background-color: white;
        border-radius: 50%;
        z-index: 0;
    }

    .circle span {
        position: relative;
        z-index: 1;
    }
</style>

<div class="circle" style="--percentage: {percentage}">
    <span>{percentage}%</span>
</div>
 -->


 <!-- CircularProgress.svelte (using it directly in the same file) -->
<script>
    export let percentage = 0;

    // Example data for testing within the same file
    let examplePercentages = [20, 40, 60, 80, 100];
</script>

<style>
    .dashboard {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 20px;
        padding: 20px;
    }

    .circle {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        background: conic-gradient(
            #4caf50 calc(var(--percentage) * 1%),
            #ccc 0
        );
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 24px;
        color: #4caf50;
        position: relative;
        margin: 10px;
    }

    .circle::before {
        content: "";
        position: absolute;
        top: 10px;
        left: 10px;
        right: 10px;
        bottom: 10px;
        background-color: white;
        border-radius: 50%;
        z-index: 0;
    }

    .circle span {
        position: relative;
        z-index: 1;
    }
</style>

<div class="dashboard">
    {#each examplePercentages as percentage}
        <!-- Each instance of the circular progress -->
        <div class="circle" style="--percentage: {percentage}">
            <span>{percentage}%</span>
        </div>
    {/each}
</div>
