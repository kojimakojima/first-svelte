<script lang="ts">
  let count: number = 0;
  let count1: number = 0;
  let numToAdd: number = 1;
  let some: string = "";
  let fruits = ["🍏 Apple", "🍌 Banana", "🍒 Cherry", "🍊 Orange"];

  const increment = () => {
    count += 1;
  };
  const decrement = () => {
    count -= 1;
  };
  const increment1 = (n: number = 1) => {
    numToAdd === undefined ? (count1 += n) : (count1 += numToAdd);
  };
  const decrement1 = (n: number = 1) => {
    numToAdd === undefined ? (count1 -= n) : (count1 -= numToAdd);
  };
  const swap = () => {
    let temp = fruits.shift()!;
    fruits.push(temp);
    fruits = fruits;
  };
</script>

<p>Value: {some}</p>
<input type="text" placeholder="here" bind:value={some} />
<hr class="my-4" />

<p>Count: {count}</p>
<button on:click={increment} class=" bg-purple-800 p-2"> + </button>
<button on:click={decrement} class="bg-sky-800 p-2"> - </button>
<hr class="my-4" />

<p>Count: {count1}</p>
<p>Num to add: {numToAdd}</p>
<input type="number" placeholder="Type num to inc/dec" bind:value={numToAdd} />
<button on:click={() => increment1()} class="bg-purple-800 p-2"> + </button>
<button on:click={() => decrement1()} class="bg-sky-800 p-2"> - </button>
<hr class="my-4" />

<ul class="flex gap-2">
  {#each fruits as f, i}
    <li><span class="text-rose-400">#{i + 1}</span>: {f}</li>
  {/each}
</ul>
<button on:click={swap} class="rounded-sm bg-indigo-600 p-1">swap</button>
