<script>
  import wordlist from "./wordlist.js"

  let word = ""
  let result = ""

  function findWord() {
    console.log(`Searching for '${word}'...`)
    // reset 
    result = "not found"
    // search the word list for the word.
    for (let i = 0; i < wordlist.length; i++ ) {
        if (wordlist[i] === word) {
            result = `Found it!`;
        }
    }
  }
</script>

<h1>Password Finder</h1>

<label>
	Find:
	<input type="text" bind:value={word}>
</label>

<button on:click={findWord}>Find</button>

<h2 class="subtitle">Result</h2>
<p>{result}</p>
