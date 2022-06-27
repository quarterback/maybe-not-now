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

</p>
<h2> Public interest design director, skeeball champ & (occasional) tennis coach</h2>
Ron Bronson is a design leader & practitioner. He currently works as Director of Design at 18F, a development & design consultancy inside the federal government. He's worked on projects with Centers of Medicare & Medicaid, Department of Defense, and others. Prior to joining 18F in 2017, he spent over a decade leading large-scale digital initiatives for public & private sector entities around the country.

Since 2007, he's been on stage at events around the world including Service Design Network, Code for America summit, An Event Apart, DrupalCon & Confab. He's given talks at events far and wide including design & tech events in South Africa, Canada, and Norway. Ron's talks focus primarily on service design, friction, so-called 'dark' patterns, and the responibility of designers.

Ron was previously a Portland Historic Landmarks Commissioner, founding director of Indianapolis Design Week, on the board of the Indianapolis chapter of AIGA, and a board member and volunteer radio news anchor at WFHB-FM, a community radio station in Bloomington, Indiana, and served in the U.S. Air Force.

Outside of work, he's a world-class skeball player, (accidentally) invented a sport in 2004, and coaches high school tennis in his spare time. Ron is also (probably) America's foremost authority on the [Finnish sport of Pesäpallo](https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa/).

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
