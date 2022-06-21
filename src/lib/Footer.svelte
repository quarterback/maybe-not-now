<script>
	import { variables } from '$lib/variables';
</script>

<footer>
	<p>
		<a href="https://twitter.com/{variables.twitter}" target="_blank" rel="noopener noreferrer"
			>Twitter
		</a>
		<a href={variables.github} target="_blank" rel="noopener noreferrer">GitHub </a>
		<a href="https://instagram.com/ronbronson" target="_blank" rel="noopener noreferrer">Instagram</a>
		<a href="https://www.last.fm/user/omnivoreron" target="_blank" rel="noopener noreferrer">Last.fm</a>
		<a href="/rss.xml" rel="external">📰 RSS </a>
	</p>
	<p>
	
	</p>
</footer>

<style>
	footer {
		width: 100%;
		margin-top: auto;
		margin-bottom: var(--space-narrow);

		text-align: center;
	}
	p,
	a {
		font-size: 90%;
		text-decoration: none;
		margin-bottom: 0;
	}

	a:hover,
	a:focus {
		text-decoration: underline;
	}
</style>
