<script>
import { currentPage } from "./store";
import About from "./about.svelte";
import Project from "./projects.svelte";
import Contact from "./contact.svelte";
import Home from "./first.svelte";
	function nav(page) {
		currentPage.set(page);
	}
	let page;
	currentPage.subscribe(value=>{
		page=value;
	});
</script>

<div class="bar">
	<div class="bar">
		<nav class="nav-title">
			<span class="textwhite"
				>Welcome to
				<span class="textred"> 4f Builders &amp; Engineering Pvt. Ltd</span>
			</span>
		</nav>
	</div>
	<nav class="nav-bar">
		<a href="#top" class="nav-link" on:click={()=>{nav('home')}}>Home</a>
		<a href="#top" class="nav-link" on:click={()=>{nav('about')}}>About us</a>
		<a href="#top" class="nav-link" on:click={()=>{nav('project')}}> Our Projects</a>
		<a href="#top" class="nav-link" on:click={()=>{nav('contact')}}>Contact Us</a>
		<!--<div class="fun">(Hover Over the title)</div>-->
	</nav>
</div>

{#if page==='home'}
	<Home />
{:else if page==='about'}
	<About />
{:else if page==='project'}
	<Project />
{:else if page === 'contact'}
	<Contact />
{/if}
<footer>
	<div class="bottom">
		<nav class="nav-bar2">
			
			<div class="image-logo">
				<span class="bottom2">This website was created using  </span>	<img src="logo.jpg" alt="" width="80" height="30" />
			</div>
			<span class="bottom2"> Webmaster: Shiva Surendran</span>
			<p class="bottom2">©copyleft 2024. all rights reserved</p>
		</nav>
	</div>
</footer>

<style>
	.bar {
		overflow: hidden;
		background-color: #fff2f2;
		text-align: left;
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
	}

	.nav-bar {
		overflow: hidden;
		background-color: #333;
		font-size: 20px;
		padding: 10px;
	}
	.nav-bar2 {
		overflow: hidden;
		background-color: #333;
		font-size: 20px;
		padding-bottom: 12px;
		padding-top: 12px;
	}


	.nav-link {
		border-radius: 5px;
		float: left;
		color: white;
		text-align: center;
		padding: 14px 16px;
		text-decoration: none;
		font-family: merriweather;
	}
	.nav-title {
		margin-bottom: 50px;
		margin: 30px;
	}

	.nav-link:hover {
		background-color: #6c7f09;
		transition: 0s;
	}

	.textwhite {
		font-size: 50px;
		margin: 0;
		font-family: poppins;
		color: rgb(0, 0, 0);
	}

	.textred {
		font-size: 50px;
		margin: 0;
		font-family: poppins;
		color: rgb(0, 0, 0);
	}



	.nav-title:hover .textred,
	.bar {
		background-color: rgb(255, 255, 255);
		color: rgb(0, 0, 0);
		font-weight: 500;
	}


	.bottom {
		text-align: center;
		color: wheat;
		font-family: Hind SILIGURI;
		font-size: 15px;
		padding: 0px;
	
	}
	
.bottom2{font-size: 13;
	font-family: Hind SILIGURI;
}
	.image-logo {
		padding: 10px;
		display: flex;
		align-items: center;
		justify-content: center;
	}
</style>
