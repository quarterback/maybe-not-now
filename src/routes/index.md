<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */
	export async function load({ fetch }) {
		const res = await fetch(`/posts.json`);
		const posts = await res.json();

		return {
			props: {
				posts
			}
		};
	}
</script>

<script>
	import Seo from '$lib/Seo.svelte';
	import BlogSummary from '$lib/BlogSummary.svelte';
	import { variables } from '$lib/variables';
	export let posts;

	const postsToShow = 3;
	$: blogPosts = posts.slice(0, postsToShow);
</script>

<!-- TODO UPDATE THE SEO INFO -->
<Seo title="Ron Bronson" description={variables.siteDescription} path="/" openGraphImage=""/>

# Ron Bronson

<p>I'm Head of Design at <a href="https://18f.gsa.gov">18F</a>
Outside of my work leading one of the government's largest in-house design teams, I speak and write on service design, information architecture & content strategy. 
In my spare time, you can find me playing skeeball, <a href="https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa/">studying Finnish</a>, or coaching a state title winning <a href="https://www.oregonlive.com/highschoolsports/2022/05/catlin-gabel-sweeps-class-4a3a2a1a-tennis-team-titles.html#:~:text=The%20Catlin%20Gabel%20Eagles%20came,reached%20the%20summit%20in%202022.">high school tennis team.</a>

<h3>Speaking</h3>
<a href="https://vimeo.com/651801535">IxDA Oslo</a>
<a href="https://www.surfacingpodcast.com/ron-bronson-transcript">Surfacing Podcast</a> - On Service Design
<a href="https://open.spotify.com/episode/3Xd9MZ9HdByErb41jb7vUX">ACT-IAC Podcast</a> - Edge Cases & Empathy
<a href="https://youtu.be/JqguCFiY3KM">Service Design Network Global Conference</a>
<a href="https://aneventapart.com/event/online-0720#s24059">An Event Apart</a>
<a href="https://www.youtube.com/watch?v=REUJCWpFOcI">DrupalCon</a>


<h3>Connect</h3>
<a href="mailto:contact@ronbronson.com">Email</a>
<a href="https://twitter.com/ronbronson">Twitter</a>
<a href="https://linkedin.com/in/ronbronson">Linkedin</a>
<a href="https://ronbronson.medium.com/">Medium</a>
<a href="https://last.fm/user/omnivoreron">Last.fm</a>
<a href="https://open.spotify.com/user/ronbronson?si=5ad7335e796f4535">Spotify</a>

<!--

## [Recent blog posts](/blog)

{#each blogPosts as blogPost}
<BlogSummary {blogPost} />
{/each} 
-->
