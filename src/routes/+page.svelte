
<script>
    import Logo from '$lib/images/Logo.png';
    import Bell from '$lib/images/Bell.png';
    import Menu from './menu.svelte';
    import TopBar from './topBar.svelte';
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


    
    
</style>

<div class="grid-container">
    <div class="grid-item boxRed centre">
        <img src = {Logo} alt = "logo">
    </div>
    <div class="grid-item boxRed"> <TopBar /> </div>
    <div class="grid-item boxRed"> <Menu /> </div>
    <div class="grid-item boxRed">
        <p> main section</p>
    </div>
    
  </div>
