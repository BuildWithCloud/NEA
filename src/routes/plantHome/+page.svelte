<script>
    import Logo from '$lib/images/Logo.png';
</script>
<style>
    .grid-container {
        display: grid;
        grid-template-columns: 14% 86% ; /* Sets the width of two columns */
        grid-template-rows: 9.7VH 90.3VH; /* Sets the height of two rows */
  
}
    .menu {
        display:grid;
        grid-template-columns:100%;
        grid-template-rows: 10% 10% 10% 10% 10%;
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
    

</style>

<div class="grid-container">
    <div class="grid-item boxRed centre">
        <img src = {Logo} alt = "logo">
    </div>
    <div class="grid-item boxRed">
        <p> Search etc</p>
    </div>
    <div class="grid-item boxRed menu">
        <div class="boxBlue centre">
            <button type="button">My Tasks</button>
        </div>
        <div class="boxBlue centre">
            <button type="button">My Plants</button>
        </div>
        <div class="boxBlue centre">
            <button type="button">All Plants</button>
        </div>
        <div class="boxBlue centre">
            <button type="button">Wish List</button>
        </div>
        <div class="boxBlue centre">
            <button type="button">Available to Harvest</button>
        </div>
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