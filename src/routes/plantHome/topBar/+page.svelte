
<script>
    import Bell from '$lib/images/Bell.png';
</script>
<style>
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
    .topBarGrid{
        display: grid;
        grid-template-columns: 45% 40% 5% 10%;
        grid-template-rows: 100%;
    }
    .profileIcon{
        height: 60px;
        width: 60px;
        border-radius: 50%;
        background-color: var(--color-tailwind500);
    }
    
</style>
<div class="topBarGrid ">
    <div class="boxBlue"> </div>
    <div class="boxBlue"> </div>
    <div class="boxBlue centre">
        <img src = "{Bell}" alt = "Notification Bell">
    </div>
    <div class="boxBlue centre">
        <span class = "profileIcon"></span>
    </div>

</div>