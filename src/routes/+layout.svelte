<script lang="ts">
	let { children } = $props();
	import '../app.css'

</script>

<nav class=" h-15 w-7 pt-0">
	<!-- put hidden back in this  -->
	 <div class="fixed top-0 left-0 w-full z-10 flex h-20 justify-center items-center content-center">
		<div class= "mt-2 border-4 bg-white navbar-center content-center items-center justify-center min-w-[500px] lg:flex w-10 h-15 rounded-[50px] border border-solid border-bg-neutral-900" >
		  <ul class="menu menu-horizontal px-1">
			<li class="text-lg"><a href = '/contact' target = '_blank'>Contact Me</a></li>
			<li><a class="text-lg" href = 'http://www.linkedin.com/in/jagroop-s-sam18731' target="_blank">LinkedIn</a></li>
			<li><a class="text-lg" href = '/resume.pdf' target='_blank'>Resume</a></li>
		</ul>
		</div>
	  </div>
	

</nav>

{@render children()}


  

