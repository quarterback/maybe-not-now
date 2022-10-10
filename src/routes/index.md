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
Outside of tech, Ron has coached tennis programs in his spare time around the country including summer camp programs throughout New England intermittently over a decade.

As Head Girls Varsity Tennis Coach at Catlin Gabel, his 2022 team won the 4A/3A/2A/1A Oregon State championship and claimed back-to-back District & Conference championships. In three seasons, he's had 11 All-District selections, as well as back-to-back individual singles & doubles district champions. While coaching in Wyoming, he led Cheyenne Central's girls team to a 3rd place finish at state, and a South Regional & Conference title. "

His boys team also finished 3rd in the region and the program boasted 2 All-State selections & 7 players All-Conference. In one season at Oregon City HS, his boys team earned OSAA All-State Academic honors. He's also coached collegiately in Illinois and high school programs in Colorado.

Ron’s career dual meet record as a head coach is currently 43-18-1, with a state championship, 3 regional titles & 3 conference titles. 

As a player, Ron was a four-year letter winner, captain & all-area doubles honorable mention selection his senior year at Plainfield (NJ) High School, where he was part of three consecutive NJSIAA state playoff teams and a conference championship in 1997, which was the first boys tennis conference title in school history. He played one season of college tennis at Monmouth (IL) College in 2003, where he played both singles (4/5/6) & doubles (2) and served as a team captain.

(He also coached college speech & debate for three seasons, (and started at least two college debate programs, and ghostwrote a student government constitution,) but now he just occasionally a new generation of debaters to his odd judging philosophy.)

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