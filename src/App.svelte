<script>
	import Book from "./Book.svelte";
	import Button from "./button.svelte";

	let title = "";
	let price = 0;
	let description = "";
	const setTitle = (e) => {
		title = e.target.value;
	};

	let books = [];

	const addBook = () => {
		const newBook = {
			title: title,
			price: price,
			description: description,
		};

		books = books.concat(newBook);
	};
</script>

<main>
	<section>
		<h1>Book Store</h1>
		<div>
			<label for="title">Title</label>
			<input type="text" id="title" value={title} on:input={setTitle} />
		</div>
		<div>
			<label for="price">Price</label>
			<input type="number" id="price" bind:value={price} />
		</div>
		<div>
			<label for="description">Description</label>
			<textarea rows="3" id="description" bind:value={description} />
		</div>

		<Button on:click={addBook}>ADD Book</Button>

		<h2>Stock</h2>

		{#if books.length === 0}
			<p>No books in store</p>
		{:else}
			{#each books as { title, price, description }}
				<Book
					bookTitle={title}
					bookPrice={price}
					bookDescription={description}
				/>
			{/each}
		{/if}
	</section>
</main>

<style>
	main {
		padding: 2rem 1.5rem;
	}

	section {
		margin: auto;
		width: 100%;
		max-width: 30rem;
	}

	h1 {
		text-align: center;
	}

	label,
	input,
	textarea {
		width: 100%;
	}
</style>
