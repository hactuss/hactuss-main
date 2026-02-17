<script>
</script>

<main>
    <div class="grid">
        <div class="col cr" data-index="1">
            <h4>creative</h4>
            <ul>
                <li>art (ng)</li>
                <li>video editing (yt)</li>
            </ul>
        </div>
        <div class="col pr" data-index="2">
            <h4>productive</h4>
            <ul>
                <li>personal organization (obsidian)</li>
                <li>office</li>
                <li>ability farming</li>
            </ul>
        </div>
        <div class="col ft" data-index="3">
            <h4>free time</h4>
            <ul>
                <li>linux rice</li>
                <li>splatoon</li>
                <li>boredom</li>
            </ul>
        </div>
        <div class="col st" data-index="4">
            <h4>state</h4>
            <ul>
                <li>future</li>
                <li>selfhosting</li>
            </ul>
        </div>
    </div>
    <div class="topic-content"><p>story</p></div>
</main>

<style>
    .grid {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: repeat(4, 1fr);
        column-gap: 2%;
        margin: 1%;
    }

    .col {
        border: solid white 1px;
        border-image: linear-gradient(rgba(255, 0, 0, 1), rgba(0, 0, 0, 0)) 1;
        border-radius: 100%;

        min-height: 100px;
    }
</style>
