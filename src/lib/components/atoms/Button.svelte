<script>
	export let kind = 'secondary';
	$: type = 'button-' + kind;
	export let href = '#';
	export let fontsize = '1.2rem';

</script>

<button class={type} style="font-size: {fontsize};" href="{href}">
		<slot/>
</button>

<style>


	button,
	.button-secondary {
		
		font-weight: 600;
		color: var(--white);
		color: var(--white);
		text-decoration: none;
		border: none;
		border-radius: 200px;
		padding: 12px 35px;
		cursor: pointer;
		background-color: transparent;
		transition: transform 0.4s var(--bezier-one), box-shadow 0.4s var(--bezier-one);
		user-select: none;
	}

	.button-primary {
		border: 1.5px solid var(--red);
		background-color: var(--red);
		box-shadow: 0px 0px 32px 1px var(--red-glow);
		color: #003258;
	}

	.button-primary:hover {
		box-shadow: 0px 0px 32px 1px var(--red-glow), 0px 0px 32px 1px var(--red-glow);
	}

	button:hover {
		transform: translateY(-5%);
	}
	button:active {
		transition-duration: 0.1s;
		transform: translateY(-3%);
	}
</style>
