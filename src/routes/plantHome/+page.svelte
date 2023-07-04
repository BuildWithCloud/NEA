<script>
    import Logo from '$lib/images/Logo.png';
    import Bell from '$lib/images/Bell.png';
    import Menu from './menu/+page.svelte';
</script>
<style>
    .grid-container {
        display: grid;
        grid-template-columns: 14% 86% ;
        grid-template-rows: 9.7VH 90.3VH;
    }
    

    .boxRed {
        border-width: 2px;
        border-style: solid;
        border-color: red;
    }
    .boxBlue{
        border-width: 2px;
        border-style: solid;
        border-color: blue;
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

    .profileIcon{
        height: 70px;
        width: 70px;
        border-radius: 50%;
        background-color: var(--color-tailwind500);
    }
    
</style>

<div class="grid-container">
    <div class="grid-item boxRed centre">
        <img src = {Logo} alt = "logo">
    </div>
    <div class="grid-item boxRed centre topBarGrid">
        <div class="boxBlue"> 
            
        </div>
        <div class="boxBlue"></div>
        <div class="boxBlue centre">
            <img src = "{Bell}" alt = "Notification Bell">
        </div>
        <div class="boxBlue centre">
            <span class = "profileIcon"></span>
        </div>

    </div>
    <div class="grid-item boxRed">
        <Menu />
    </div>
    <div class="grid-item boxRed">
        <p> main section</p>
    </div>
    
  </div>
<h1>
    Welcome to the start of an epic journey!
</h1>

<p>
    I am designing a plant database and this is the future home page
</p>