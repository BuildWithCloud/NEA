<script lang='ts'>
     let selectedButton: HTMLButtonElement | null = null;

     function selectButton(event: Event){
        if(selectedButton){
            selectedButton.dataset.selected = "false";
        }
        selectedButton = event.target as HTMLButtonElement;
        selectedButton.dataset.selected = "true";
    }
</script>

<style>
    .menu{
        display:grid;
        grid-template-columns:100%;
        grid-template-rows: 50px 50px 50px 50px 50px;
    }
    .centre{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .boxBlue{
        border-width: 2px;
        border-style: solid;
        border-color: blue;
    }
    button, .menuButton{
        background-color: var(--color-tailwind100);
        border-color: var(--color-tailwind100);
        width: 100%;
        height: 100%;
        color: var(--color-tailwind900);
    }

    .menuButton[data-selected="true"]{
        background-color: var(--color-brand500);
        border-color: var(--color-brand500);
        
    }
    .menuButton[data-selected="false"]{
        background-color: var(--color-tailwind100);
        border-color: var(--color-tailwind100);
        
    }
</style>
<div class = "menu">
    <div class="boxBlue centre">
        <button type="button" class="menuButton" data-selected="true" bind:this={selectedButton} on:click={selectButton}>My Tasks</button>
    </div>
    <div class="boxBlue centre">
        <button type="button" class="menuButton" on:click={selectButton}>My Plants</button>
    </div>
    <div class="boxBlue centre">
        <button type="button" class="menuButton" on:click={selectButton}>All Plants</button>
    </div>
    <div class="boxBlue centre">
        <button type="button" class="menuButton" on:click={selectButton}>Wish List</button>
    </div>
    <div class="boxBlue centre">
        <button type="button" class="menuButton" on:click={selectButton}>Available to Harvest</button>
    </div>
</div>