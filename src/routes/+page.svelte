<script>
    let content = $state("default");
    let story = $state("");

    function setDefault() {
        content = "default";
    }
</script>

<main>
    <div>
        <p>Hello, my [psydonym] is Hactuss.</p>
    </div>
    <div class="flex">
        <div class="hea">creative</div>
        <div class="hea">productive</div>
        <div class="hea">free time</div>
        <div class="hea">state</div>
    </div>
    <div class="grid">
        <div
            class="col cr"
            on:mouseenter={() => {
                content = "creative";
            }}
            on:mouseleave={() => {
                setDefault();
            }}
        >
            <h4>creative</h4>
            <ul>
                <li>art (ng)</li>
                <li>video editing (yt)</li>
            </ul>
        </div>
        <div
            class="col pr"
            on:mouseenter={() => {
                content = "productive";
            }}
            on:mouseleave={() => {
                setDefault();
            }}
        >
            <h4>productive</h4>
            <ul>
                <li>personal organization (obsidian)</li>
                <li>office</li>
                <li>ability farming</li>
            </ul>
        </div>
        <div
            class="col ft"
            on:mouseenter={() => {
                content = "free time";
            }}
            on:mouseleave={() => {
                setDefault();
            }}
        >
            <h4>free time</h4>
            <ul>
                <li>linux rice</li>
                <li>splatoon</li>
                <li>boredom</li>
            </ul>
        </div>
        <div
            class="col st"
            on:mouseenter={() => {
                content = "state";
            }}
            on:mouseleave={() => {
                setDefault();
            }}
        >
            <h4>state</h4>
            <ul>
                <li>future</li>
                <li>selfhosting</li>
            </ul>
        </div>
    </div>
    <div class="topic-content">
        <h2>{content}</h2>
        <p>
            {story}
        </p>
    </div>
</main>

<style>
    :root {
        --cr-color: rgba(255, 0, 0, 1);
        --pr-color: rgba(255, 0, 0, 1);
        --ft-color: rgba(255, 0, 0, 1);
        --st-color: rgba(255, 0, 0, 1);
    }
    * {
        accent-color: purple;
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: repeat(4, 1fr);

        grid-template-areas: "";
        column-gap: 2%;
        margin: 1%;
    }
    /*
    .grid {
        column-count: 4;
    }*/

    .col {
        border: solid;
        min-height: 200px;
        width: 100%;
    }
    .cr {
        border-image: linear-gradient(var(--cr-color), rgba(0, 0, 0, 0)) 1;
    }
    .pr {
        border-image: linear-gradient(var(--pr-color), rgba(0, 0, 0, 0)) 1;
    }
    .ft {
        border-image: linear-gradient(var(--ft-color), rgba(0, 0, 0, 0)) 1;
    }
    .st {
        border-image: linear-gradient(var(--st-color), rgba(0, 0, 0, 0)) 1;
    }
    .flex {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
    }
</style>
