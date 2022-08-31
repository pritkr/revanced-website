<script>
	export let src = 'socials/github.svg';
	export let alt = 'GitHub';
	export let href = '#';
</script>

<div>
	<button href={href}>
			<img {src} {alt} />
	</button>
</div>

<style>
	button {
		border: 0;
		width: 60px;
		height: 60px;
		padding: 14px;
		cursor: pointer;
		border-radius: 20px;
		transition: all 0.4s var(--bezier-one);
		background-color: var(--grey-four);
		color: var(--white);
		user-select: none;
	}

	div {
		display: inline-block;
	}

	img {
		transition: filter 0.4s var(--bezier-one);
		width: 30px;
	}

	div:hover > button {
		transform: translateY(-5%);
		background-color: var(--grey-two);
	}

	button:hover img {
		filter: brightness(1.2);
	}
</style>
