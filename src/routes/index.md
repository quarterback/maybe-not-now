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

<h2>Design Leadership & Digital transformation</h2>

<p> My specialities are service design and information architecture. Beyond just building websites, I'm really good at helping stakeholders identify & solve intractable problems through user inquiry. Right now, I'm Head of Design for one of the largest design departments in the federal government at <a href="https://18f.gsa.gov">18F</a>. Day to day, I lead teams of managers and designers who help improve technology for the public interest. For nearly two decades, I've worn every imaginable hat you can on digital project teams -- product manager, content strategist, UX designer, researcher and product designer. 

Outside of work, you can also find me spinning up skeeball leagues, or <a href="https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa/">co-hosting the only English-language podcast about Finnish baseball.</a> (it's a long story...) 

I was appointed by the Mayor to serve on the Portland Historic Landmarks Commission; served on several boards (AIGA Indy, IxDA), and spent two years as a radio news anchor (and board member) for a community radio station. I founded Indianapolis Design Week in 2017, which still exists under different leadership. Randomly, I (accidentally) <a href="https://en.wikipedia.org/wiki/Tennis_polo">invented a sport once</a>, and many moons ago, served in US Air Force.

After playing tennis in both high school & college, I took up coaching. I worked at camps & schools around the country before taking nearly a decade off. In 2019, I started coaching high school tennis again as a head coach. My coaching philosophy mirrors how I work as a design leader; take the time to understand what motivates people, help them develop a success plan & put them in situations where they can gain confidence and grow. (Sometimes, this means failing first.) I run an inclusive program that motivates kids at every level to grow, regardless of their spot on the challenge ladder.

<h3>Tennis Honors</h3>
<p>
2022 OSAA 4A/3A/2A/1A Girls Tennis State Champions (Catlin Gabel School)<br>
2022 District Girls Tennis Coach of the Year<br>
2021 & 2022 District Champions, 2x League Championships (20-0 in league play since 2019)<br>
12x All-District selections (2021-22), 4x individual district champions <br>
2019 OSAA All-State Academic Team (Oregon City HS)<br></p>


<h3>Speaking</h3>
<p>I've been on stage at over 50 tech & design conference since 2013. Beyond local events, I've been on stage at global events like Service Design Global Conference, Confab, An Event Apart and Pixel Up. I speak on a range of topics related to my work, and enjoy melding technical expertise with practical realness for audiences used to more staid talks. My energy on stage is consistently a hit. I've also been a guest on a number of industry podcasts, and have been a tech mentor & guest speaker for a host of student groups. 
</p>

<h3>Talks</h3>
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
<a href="https://glass.photo/ron">Instagram</a>
<a href="https://open.spotify.com/user/ronbronson?si=5ad7335e796f4535"><i class="fa-brands fa-spotify"></i></a>

<!--

## [Recent blog posts](/blog)

{#each blogPosts as blogPost}
<BlogSummary {blogPost} />
{/each} 
-->