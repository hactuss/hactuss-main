<script>
    let content = $state("default");
    let story = $state("");

    function setDefault() {
        content = "default";
    }
    let scrollText1 = $state("71");
    let scrollText2 = $state("72");
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

    <div>
        <h1>moing text</h1>
        <div style:overflow="hidden">
            <p class="marquee">
                <span>1 2 3 4 5 6 7 8 9 0</span>
            </p>
            <p class="marquee2">
                <span>&#160 1 2 3 4 5 6 7 8 9</span>
            </p>
        </div>
    </div>
    <div class="stc">
        <p class="st one">{scrollText1}</p>
        <p class="st two">{scrollText2}</p>
    </div>
</main>

<style lang="scss">
    .marquee {
        margin: 0 auto;
        white-space: nowrap;
        overflow: hidden;

        border: solid red 1px;
        width: 100%;
    }

    .marquee span {
        display: inline-flex;
        padding-left: 100%;
        animation: marquee 10s linear infinite;
    }
    .marquee2 {
        margin: 0 auto;
        white-space: nowrap;
        overflow: hidden;
        border: solid red 1px;
        width: 100%;
    }
    .marquee2 span {
        display: inline-flex;
        padding-left: 100%;
        animation: marquee 10s linear infinite;
    }
    @keyframes marquee {
        0% {
            transform: translate(0, 0);
        }
        100% {
            transform: translate(-100%, 0);
        }
    }
    @keyframes marquee2 {
        0% {
            transform: translate(0, 0);
        }
        100% {
            transform: translate(-100%, 0);
        }
    }
    /*{
        animation: scrolling-text 1s linear infinite;
    }*/
    .stc {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-shrink: 0;
        overflow-y: hidden;
    }
    .st {
        margin: 2%;
        border: solid red 1px;
        text-align: center;
    }
    .one {
        flex: 1;
        animation: flex-one 3s infinite linear;
        width: 100px;
        text-align: center;
    }
    .two {
        flex: 0;
        animation: flex-two 3s infinite linear;
        width: 100px;
        text-align: center;
    }
    @if (flex = 0) {
        display: none;
    }

    @keyframes flex-one {
        from {
            flex: 1;
        }
        to {
            flex: 0;
        }
    }
    @keyframes flex-two {
        from {
            flex: 0;
        }
        to {
            flex: 1;
        }
    }
    @keyframes scrolling-text {
        from {
            transform: translateX(00%);
        }
        to {
            transform: translateX(-100%);
        }
    }

    :root {
        --cr-color: rgba(255, 0, 0, 0.3);
        --pr-color: rgba(255, 0, 0, 0.3);
        --ft-color: rgba(255, 0, 0, 0.3);
        --st-color: rgba(255, 0, 0, 0.3);
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
