<script>
	import WordComponent from "./WordComponent.svelte";
	export let response = false;

	export let wordbook = [
		{word: 'apple', translation: 'яблоко', incorrect: 0},
		{word: 'work', translation: 'работа', incorrect: 0},
		{word: 'walk', translation: 'идти', incorrect: 0},
		{word: 'read', translation: 'читать', incorrect: 0},
		{word: 'book', translation: 'книга', incorrect: 0},
		{word: 'spring', translation: 'весна', incorrect: 0},
		{word: 'lesson', translation: 'урок', incorrect: 0},
		{word: 'promise', translation: 'обещание', incorrect: 0},
		{word: 'component', translation: 'компонент', incorrect: 0},
		{word: 'language', translation: 'язык', incorrect: 0},
		{word: 'pen', translation: 'ручка', incorrect: 0},
		{word: 'phone', translation: 'телефон', incorrect: 0},
		{word: 'task', translation: 'задача', incorrect: 0},
	];

	export let word = wordbook[0];

	function randomWord() {
		word =  wordbook[Math.ceil(Math.random() * 10)];
	}

	function toggleWord() {
		response = !response;
	}

	$: getWord = response ? word.word : word.translation;

</script>

<main>
	<h1>Hello {getWord}!</h1>
	<WordComponent on:click={toggleWord} word={getWord} />
	<button on:click={randomWord}>Дальше</button>
</main>

<style>
main {
	height: 100%;
}
</style>