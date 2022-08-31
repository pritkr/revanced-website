<script>

import Button from "$lib/components/atoms/Button.svelte";
import NavHost from "$lib/components/molecules/NavHost.svelte";
import SocialButton from "$lib/components/atoms/SocialButton.svelte";
import SocialHost from "$lib/components/molecules/SocialHost.svelte";
import Wave from '$lib/components/atoms/Wave.svelte';

</script>

<svelte:head>
	<meta charset="UTF-8" />
	<meta http-equiv="X-UA-Compatible" content="IE=edge" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Manrope:wght@200;300;400;500;600;700;800&display=swap"
		rel="stylesheet"
	/>
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">
	<meta name="og:title" content="ReVanced"/>
	<meta name="og:image" itemprop="image" content="/embed.png">
	<meta property="og:description" content="An extensible framework for building application mods.">
	<meta name="twitter:image" itemprop="image" content="/embed.png">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="theme-color" content="#0f111a">
	<title>ReVanced</title>
</svelte:head>

<NavHost></NavHost>
<slot />
<Wave />

<style>
	:global(*) {
		box-sizing: inherit;
		margin: 0;
		padding: 0;
		font-family: 'Manrope', sans-serif;
	}

	:global(html) {
		margin: 0;
		padding: 0;
		font-size: 100%;
		box-sizing: border-box;
		overflow-y: scroll;
	}

	:global(body) {
		width: 100vw;
		margin: 0;
		padding: 0;
		line-height: 1.3;
		background-color: #161c23;

	}

	:global(html, body) {
		max-width: 100%;
	}

	:global(.wrapper) {
		margin-inline: auto;
		width: min(87%, 100rem);
	}

	:root {
		--white: #fff;
		--red: #8bbaf4;		
		--grey-one: #252B31;
		--grey-two: #28313b;
		--grey-three: #3B4858;
		--grey-four: #1B1E29;
		--grey-five: #D0D0D0;
		--grey-six: #a19e9e;
		--grey-seven: #535563;
		--bezier-one: cubic-bezier(0.25, 0.46, 0.45, 0.94)
	}

	:global(::selection) {
		color: var(--white);
		background: var(--red);
	}

	/*-----headings-----*/

	:global(h1) {
		color: var(--white);
		font-weight: 700;
		letter-spacing: -0.03em;
		line-height: 0.75em;
	}

	:global(h2) {
		color: var(--white);
		font-weight: 300;
		font-size: 1.75rem;
	}

    :global(h3) {
		color: var(--white);
		font-weight: 600;
		font-size: 1rem;
    }

    :global(h4) {
		color:var(--grey-six);
        font-weight:500;
        font-size: 1rem;
    }

    :global(h5) {
		color:var(--white);
        font-weight: 300;
        font-size: 1rem;
    }

	/*-----scrollbar-----*/
	:global(::-webkit-scrollbar) {
		width: 20px;
		background-color: transparent;
	}

	:global(::-webkit-scrollbar-thumb) {
		background-color: var(--grey-three);
		border-radius: 20px;
		border: 6px solid transparent;
		background-clip: content-box;
	}

	:global(::-webkit-scrollbar-thumb:hover) {
		background-color: var(--grey-seven);
	}

	:global(input),
	:global(textarea),
	:global(button),
	:global(select),
	:global(a) {
		-webkit-tap-highlight-color: rgba(0,0,0,0);
	}
</style>
