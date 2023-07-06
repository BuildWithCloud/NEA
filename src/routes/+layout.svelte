<script lang='ts'>
	import Logo from '$lib/images/Logo.png';
	import './styles.css';
    import Bell from '$lib/images/Bell.png';
	//import Menu from './menu.svelte';
	//import Bell from '$lib/images/Bell.png';

    let searchText = '';

    let selectedButtonSearchBar: HTMLButtonElement | null = null;
    let selectedButtonMenu: HTMLButtonElement | null = null;

    let searchMyPlants: HTMLButtonElement | null = null;
    let searchAllPlants: HTMLButtonElement | null = null;
    let searchWishlist: HTMLButtonElement | null = null;
    let menuMyPlants: HTMLButtonElement | null = null;
    let menuAllPlants: HTMLButtonElement | null = null;
    let menuhWishlist: HTMLButtonElement | null = null;
    
    function selectButtonSearchBar(event: Event){
        if(selectedButtonSearchBar){
            selectedButtonSearchBar.dataset.selected = "false";
        }
        selectedButtonSearchBar = event.target as HTMLButtonElement;
        selectedButtonSearchBar.dataset.selected = "true";
    }

    function selectButtonMenu(event: Event){
        if(selectedButtonMenu){
            selectedButtonMenu.dataset.selected = "false";
        }
        selectedButtonMenu = event.target as HTMLButtonElement;
        selectedButtonMenu.dataset.selected = "true";
 
   
            if (selectedButtonMenu && selectedButtonSearchBar && searchMyPlants && selectedButtonMenu === menuMyPlants) {
                searchMyPlants.dataset.selected = "true";
                selectedButtonSearchBar.dataset.selected = "true";
            } else if (selectedButtonMenu && selectedButtonSearchBar && searchAllPlants && selectedButtonMenu === menuAllPlants) {
                searchAllPlants.dataset.selected = "true";
                selectedButtonSearchBar.dataset.selected = "true";
            } else if (selectedButtonMenu && selectedButtonSearchBar && searchWishlist && selectedButtonMenu === menuhWishlist) {
                searchWishlist.dataset.selected = "true";
                selectedButtonSearchBar.dataset.selected = "true";
            }
 }
</script>

<div class="app">
	<div class="grid-container">
		<div class="grid-item debugRed centre">
			<img src = {Logo} alt = "logo">
		</div>
		<div class="grid-item debugRed"> <div class="topBarGrid ">
			<div class="debugBlue centreVertically searchBarGrid ">
				<div class = "searchBarPadding">
					<div class = "centreVertically">
						<input type="text" class="textbox" bind:value="{searchText}" placeholder="Search" >
					</div>
				</div>
				<div class="searchButtonsGrid centreVertically fullHeight">
					<div class = "centre fullHeight">
						<button class="searchBarButton" data-selected="true" bind:this={searchMyPlants} on:click={selectButtonSearchBar}>My Plants</button>
					</div>
					<div class = "centre fullHeight">
						<button class="searchBarButton" data-selected="false" bind:this={searchAllPlants} on:click={selectButtonSearchBar}>All Plants</button>
					</div>
					<div class = "centre fullHeight">
						<button class="searchBarButton" data-selected="false" bind:this={searchWishlist} on:click={selectButtonSearchBar}>Wishlist</button>
					</div>
		
				</div>
					 
			</div>
			<div class="debugBlue"> </div>
			<div class="debugBlue centre">
				<img src = "{Bell}" alt = "Notification Bell">
			</div>
			<div class="debugBlue centre">
				<span class = "profileIcon"></span>
			</div>
		
		</div> </div>
		<div class="grid-item debugRed menu"> <div class="boxBlue centre">
			<button type="button" class="menuButton" data-selected="true" bind:this={selectedButtonMenu} on:click={selectButtonMenu}>My Tasks</button>
		</div>
		<div class="boxBlue centre">
			<button type="button" class="menuButton" bind:this={menuMyPlants} on:click={selectButtonMenu}>My Plants</button>
		</div>
		<div class="boxBlue centre">
			<button type="button" class="menuButton" on:click={selectButtonMenu}>All Plants</button>
		</div>
		<div class="boxBlue centre">
			<button type="button" class="menuButton" on:click={selectButtonMenu}>Wish List</button>
		</div>
		<div class="boxBlue centre">
			<button type="button" class="menuButton" on:click={selectButtonMenu}>Available to Harvest</button>
		</div> </div>
		<div class="grid-item debugRed">
			<p> main section</p>
		</div>
		
	  </div>
	
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}
	.grid-container {
        display: grid;
        grid-template-columns: 14% 86% ;
        grid-template-rows: 9.7VH 90.3VH;
    }
    
    .centre{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    
    
    .topBarGrid{
        display: grid;
        grid-template-columns: 45% 40% 5% 10%;
        grid-template-rows: 100%;
    }

	.centre{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .centreVertically{
        display: flex;
        align-items: center;
        
    }
    
    .topBarGrid{
        display: grid;
        grid-template-columns: 50% 35% 5% 10%;
        grid-template-rows: 9.5VH;
    }
    .searchBarGrid{
        display: grid;
        grid-template-columns: 35% 65%;
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

    .searchBarButton{
        height: 80%;
        width:100%;
        font-family: PT Sans, sans-serif;
        font-size: 130%;
        color: var(--color-tailwind900);
    }
    .searchBarButton[data-selected="true"]{
        background-color: var(--color-brand500);
        border-color: var(--color-brand500);
        
    }
    .searchBarButton[data-selected="false"]{
        background-color: var(--color-tailwind400);
        border-color: var(--color-tailwind400);
        
    }
    .fullHeight{
        height: 100%;
    }


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
    
        
    
	/*debug styles*/
	.debugRed{
		border-width: 2px;
		border-style: solid;
		border-color: red;
	}
	.debugBlue{
		border-width: 2px;
		border-style: solid;
		border-color: blue;
	}
	
</style>
