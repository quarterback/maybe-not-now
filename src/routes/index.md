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

<p>I'm Head of Design at <a href="https://18f.gsa.gov">18F</a>. I've spent my career working on large-scale digital transformation, and working with cross-functional teams on iterative software delivery. 

In practice, I wear a lot of hats. Everything from leading a team of design managers, hiring, performance reviews, and lots of meetings helping advise and steer the direction of our work on behalf of the public. 

Hands on, I've led content strategy & information architecture; steered UX research; advised senior leaders on digital strategy; and occasionally some Agile product management. 

I speak globally on these topics, too. I'm also (very slowly) working on a book about Consequence Design.

<h3>Extracurriculars</h3>

Outside of work, you can find me playing skeeball, <a href="https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa/">studying Finnish</a>, or coaching <a href="https://www.oregonlive.com/highschoolsports/2022/05/catlin-gabel-sweeps-class-4a3a2a1a-tennis-team-titles.html#:~:text=The%20Catlin%20Gabel%20Eagles%20came,reached%20the%20summit%20in%202022.">high school tennis.</a>

Previously, I served on the Portland Historic Landmarks Commission, was an AIGA Indianapolis board member, a radio news anchor (and board member) for a community radio station. I also started Indianapolis Design Week in 2017.

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