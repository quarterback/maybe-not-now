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

<p class=emph>
Public interest design leadership, service designer, tennis coach & skeeball champ.
</p>

<h2>I work at 18F part of the federal government's Technology Transformation Services. As Head of Design, I manage one of the largest in-house design teams in the federal government, deploying designers as part of cross-functional teams to collaborate with federal (and sometimes, state) agencies on improving service delivery.</h2>

Prior to joining senior leadership at 18F, I served as a design manager, staffing lead, and individual contributor on engagements with agencies with the Centers for Medicare & Medicaid, Department of Defense, Federal Trade Commission, and others. 

Before joining the federal government, I spent years working across local & state government wearing a lot of hats, but mostly leading large-scale digital transformation projects. My core skills are information architecture, service design, UX research, and content strategy. 

Many moons ago, I also served in the U.S. Air Force.

<h3> Coaching </h3>

I've coached high school (and one college) tennis teams in Oregon & Colorado intermittently since 2009. 

Right now, I'm Head Girls Varsity Tennis coach at Catlin Gabel School in Portland. We won the Oregon 4A state title this past year (which was pretty cool.)

I played college & high school tennis and had a coach that changed my life. It inspired me to coach, so I spent several summers at camps as a tennis coach. [I talked about this on a podcast, once.](https://podcasts.apple.com/fi/podcast/2-mr-van-blake-pes%C3%A4pallo-consequence-design-with-ron/id1543988908?i=1000523670103)


<h3> Volunteering </h3>

In 2021-22, I served on the Portland Historic Landmarks Commission, which mostly happened because I have an instagram that's just neon photos.

Other semi-interesting stuff I've done: I started Indianapolis Design Week in 2016 and ran it for two years, before transferring leadership. (It still exists!) I've run a few other design/tech events in the past, too. 

I've launched skeeball leagues in at least two cities, too. Also, I'm (probably) America's foremost authority on the [Finnish sport of Pesäpallo.](https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa/) 

Speaking of sports, there's the time [we invented one](https://toccer.tumblr.com/). 

<!-- ## Get started

Get up and running with this site really fast! For an [opinionated
quickstart](/blog/initial-setup), you need to have

- clicked "use this template" in [GitHub]({variables.github}), so you have your own copy of
  this repository, and cloned it to your own computer
- set up a free account on Netlify ready for [deployment](/blog/deployment) (other static site hosting options
  are fine if you know how)
- thought about whether you are happy writing blog content in files in
  GitHub, or prefer to use a [CMS](/blog/cms) for web-based writing.
- thought about whether this template has the right site sections
  (home/blog/about) for you, or if you need extra pages

While this template is still under development, these docs assume that you:

- are vaguely familiar with basic git commands (clone, add, commit, push) and GitHub
- know how to edit HTML/JavaScript files on your computer (even if you don't fully
  understand what they mean)
- are able to set up a working NodeJS environment on your computer.

More comprehensive beginner documentation is coming soon, and if you get stuck feel free to [contact
us](mailto:hi@codexfelis.dev) for help or [raise an issue in GitHub]({variables.github}/issues). 

<a class=emph href="/blog/initial-setup">
Get started!
</a>

## [Recent blog posts](/blog)

{#each blogPosts as blogPost}
<BlogSummary {blogPost} />
{/each} 
-->
