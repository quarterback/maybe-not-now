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

<h2>Service Design Leadership</h2>

Ron Bronson is a design leader & strategist with deep experience leading digital initiatives from ideation to post-launch. Outside of work, he's a global speaker on service design. His practice is focused around Consequence Design which centers on interaction design harms (aka "dark patterns"), the intersection of technology in spatial experiences, and consumer advocacy in service delivery. He spent the past 4 years at GSA's 18F, most recently as head of one of the government's largest in-house design teams.

He was appointed by the Mayor to serve on the Portland Historic Landmarks Commission; was a member of several non-profit boards (AIGA Indy, IxDA) and even a community radio station. He organized the first Indianapolis Design Week in 2017, and one summer in Connecticut (accidentally) <a href="https://en.wikipedia.org/wiki/Tennis_polo">invented a sport.</a> Many moons ago, Ron served in US Air Force. <br>

Outside of work, you can also find him spinning up skeeball leagues, curating the tea menu at your favorite hangout, hosting bar trivia, podcasting, or <a href="https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa/">ranting online in Finnish</a> about baseball. (it's a long story...) <br>


<h3>Speaking</h3>

I gave my first talk when I was 5 years old and I feel like I've had a mic in my hand ever since. (Ask me the story sometime...)

Beyond local events, I've been on stage at global events like Service Design Global Conference, Confab, An Event Apart and Pixel Up. I speak on a range of topics related to my work, and enjoy melding technical expertise with practical realness for audiences used to more staid talks. My energy on stage is consistently a hit. I've also been a guest on a number of industry podcasts, and have been a mentor & guest speaker for a host of student groups.

<h3>Upcoming Talks</h3> 

FTA Tech Conference - Portland, OR (August 2022)<br />
Portland Design Festival - (October 2022)<br />
Rosenfeld Media Civic Design Conference - (November 2022) <br />

<h3>Recent Talks</h3>
<a href="https://vimeo.com/651801535">IxDA Oslo - Dec 2021</a>
<a href="https://www.surfacingpodcast.com/ron-bronson-transcript">Surfacing Podcast</a> - On Service Design (2021)
<a href="https://open.spotify.com/episode/3Xd9MZ9HdByErb41jb7vUX">ACT-IAC Podcast</a> - Edge Cases & Empathy (2021)
<a href="https://youtu.be/JqguCFiY3KM">Service Design Network Global Conference</a> (2020)
<a href="https://aneventapart.com/event/online-0720#s24059">An Event Apart</a> (2020)
<a href="https://www.youtube.com/watch?v=REUJCWpFOcI">DrupalCon</a> (2018)

<h3>Coaching</h3>

Ron has directed tennis programs at summers camps throughout New England, and coached collegiate and high school programs over the past two decades in Colorado, Illinois, Oregon and Wyoming. Since 2019, he's coached varsity HS tennis in Oregon where he's led the Catlin Gabel Girls Tennis Program to back-to-back District Championships and their first 4A-1A Girls State championship since 2016. (He also coached college debate for a spell too, but doesn't miss it.)

<li>2022 OSAA 4A/3A/2A/1A Girls Tennis State Champions (Catlin Gabel School)<br></li>
<li>2022 District Girls Tennis Coach of the Year<br></li>
<li>2021 & 2022 District Champions, 2x League Championships (20-0 in league play since 2019)<br></li>
<li>12x All-District selections (2021-22), 4x individual district champions <br></li>
<li>2019 OSAA All-State Academic Team (Oregon City HS)<br></p>

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