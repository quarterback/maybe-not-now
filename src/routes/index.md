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

<h2></h2>

I’m a Design Director based in Portland, Oregon. I’ve spent the bulk of my professional career working online, which is a wild proposition to my childhood self. Outside of technology, I run a local skeeball league, I coach high school, and nerd out on a bevy of random topics like <a href="https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa">Finnish baseball</a>. You can find me at conferences and design events around the world, or occasionally, on a podcast or two. 

I've been talking for the past few years about <a href="https://consequencedesign.org">Consequence Design</a>, eventually I'll merge that into a singular blog here but I haven't been able to get myself to do that yet. 

Want to collaborate on something? [Get in touch](mailto:coach@ronbronson.com)

<h3>Upcoming Talks</h3> 

FTA Tech Conference - Portland, OR (August 2022)<br />
Portland Design Festival - (October 2022)<br />
Federal CX Leadership Symposium - (October 2022) <br />
Cloudflare Design Growth Week - (October 2022) <br />
Rosenfeld Media Civic Design Conference - (November 2022) <br />
ConveyUX - (May 2023) <br />

<h3>Videos of Ron Talking With his Hands</h3>

Ron has presented at over 50 design & tech events around the world since 2017.

<h3>Recent Talks</h3>
<a href="https://vimeo.com/651801535">IxDA Oslo - Dec 2021</a>
<a href="https://www.surfacingpodcast.com/ron-bronson-transcript">Surfacing Podcast</a> - On Service Design (2021)
<a href="https://open.spotify.com/episode/3Xd9MZ9HdByErb41jb7vUX">ACT-IAC Podcast</a> - Edge Cases & Empathy (2021)
<a href="https://youtu.be/JqguCFiY3KM">Service Design Network Global Conference</a> (2020)
<a href="https://aneventapart.com/event/online-0720#s24059">An Event Apart</a> (2020)
<a href="https://www.youtube.com/watch?v=REUJCWpFOcI">DrupalCon</a> (2018)

<h3>Coaching</h3> 
For the past few years, I've been back coaching high school tennis. I started my coaching career right after high school, and at a few summer camps between -- and after -- college. I've coached high school tennis programs in Colorado, Wyoming & Oregon. I was a collegiate assistant for a program in Illinois once, too. My high school dual meet record is 43-18-1. As a head coach, I've led teams to a state title (2022), two regional statei 


<h3>Connect</h3>
<a href="mailto:contact@ronbronson.com">Email</a>
<a href="https://twitter.com/ronbronson">Twitter</a>
<a href="https://linkedin.com/in/ronbronson">Linkedin</a>
<a href="https://ronbronson.medium.com/">Medium</a>
<a href="https://last.fm/user/omnivoreron">Last.fm</a>
<a href="https://glass.photo/ron">Instagram</a>
<a href="https://open.spotify.com/user/ronbronson?si=5ad7335e796f4535"><i class="fa-brands fa-spotify"></i></a>

<!--

## [Recent blog posts](/blog)

{#each blogPosts as blogPost}
<BlogSummary {blogPost} />
{/each} 
-->