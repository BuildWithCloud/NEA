
<script>
    import Bell from '$lib/images/Bell.png';
    let searchText = '';
</script>
<style>
    .centre{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .centreVertically{
        display: flex;
        align-items: center;
        
    }
    .boxBlue{
        border-width: 2px;
        border-style: solid;
        border-color: blue;
    }
    .topBarGrid{
        display: grid;
        grid-template-columns: 45% 40% 5% 10%;
        grid-template-rows: 9.5VH;
    }
    .searchBarGrid{
        display: grid;
        grid-template-columns: 40% 60%;
        grid-template-rows: 100%;
        background-color: var(--color-tailwind300);
        border-width: 5px;
        border-color: var(--color-tailwind100);
        
    }
    .searchButtonsGrid{
        display: grid;
        grid-template-columns: 33% 33% 33%;
        grid-template-rows: 100%;
        background-color: var(--color-tailwind400);
        
    }
    .profileIcon{
        height: 60px;
        width: 60px;
        border-radius: 50%;
        background-color: var(--color-tailwind500);
    }
    .textbox {
    padding: 10px;
    font-size: 16px;
    border: 1px solid var(--color-tailwind300);
    border-radius: 5%;
    width: 100%;
    background-color: var(--color-tailwind300); 
    color: var(--color-tailwind600);
    font-family: PT Sans, sans-serif;
    }
    
    .searchBarPadding{
        padding: 10px;
    }

    .selectedSearchButton{
        background-color: var(--color-brand500);
        border-color: var(--color-brand500);
    }
    .unselectedSearchButton{
        background-color: var(--color-tailwind400);
        border-color: var(--color-tailwind400);
    }
    .searchBarButton{
        height: 80%;
        width:100%;
        color: var(--color-tailwind900);
    }
  
    
</style>
<div class="topBarGrid ">
    <div class="boxBlue centreVertically searchBarGrid ">
        <div class = "searchBarPadding">
            <div class = "centreVertically">
                <input type="text" class="textbox" bind:value="{searchText}" placeholder="Search" >
            </div>
        </div>
        <div class="searchButtonsGrid centreVertically">
            <div class = "centre">
                <button class="searchBarButton selectedSearchButton">My Plants</button>
            </div>
            <div class = "centre">
                <button class="searchBarButton unselectedSearchButton">All Plants</button>
            </div>
            <div class = "centre">
                <button class="searchBarButton unselectedSearchButton">Wishlist</button>
            </div>

        </div>
             
    </div>
    <div class="boxBlue"> </div>
    <div class="boxBlue centre">
        <img src = "{Bell}" alt = "Notification Bell">
    </div>
    <div class="boxBlue centre">
        <span class = "profileIcon"></span>
    </div>

</div>