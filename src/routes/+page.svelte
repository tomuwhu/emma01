<script>
const n = 10
var a = Array(300).fill(a).map( () => 
    Array(n).fill(0).map(()=> Math.floor(6 * Math.random()) + 1).reduce((a, b) => a += b)
)
var b = Array(5 * n).fill(0).map((_,i) => a.filter(x => x == i + 10).length)
</script>

    {#each b as x, j}
    <div class="r">
        <span class="h">{j + n}</span>
        {#each Array(x) as _, i}
            <span>{i + 1}</span>
        {/each}
    </div>
    {/each}
<style>
    div.r {
        height: 20px;
        margin: -7px;
        user-select: none;
    }
    span {
        display: inline-block;
        background-color: aquamarine;
        width: 15px;
        font-size: 8px;
        text-align: center;
        padding: 1px;
        margin: 1px;
        border-radius: 4px;
        border: solid 0.5px black;
    }
    span.h {
        background-color: rgb(162, 130, 193);
        color:white;
    }
</style>