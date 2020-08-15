<style>
	.green {
		background-color: green;
	}
	.red {
		background-color: red;
	}
	h1, figure, p {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}

	figure {
		margin: 0 0 1em 0;
	}

	img {
		width: 100%;
		max-width: 400px;
		margin: 0 0 1em 0;
	}

	p {
		margin: 1em auto;
	}

	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>

<svelte:head>
	<title>Testing Sapper</title>
</svelte:head>

<h1>Great success!</h1>

<figure>
	<img on:click={()=>alert(value)} alt='Sunset over water' src='photo1.jpg'>
	<figcaption>Sunset over water</figcaption>
</figure>

<script>let value = 14;</script>
<center>
	<input bind:value class:green={value >= 240} class:red={'number' != typeof(value)} type=number />
	<h2>{'number' == typeof(value) ? value : 0}</h2>
</center>

<p><strong>Testing by Mihael Mutić</strong></p>
