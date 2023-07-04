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
</style>
<div class = "menu">
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