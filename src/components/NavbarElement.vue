<template>
    <!-- Navbar start -->
    <nav class="w-screen fixed bg-opacity-90 bg-white p-4 lg:px-20 flex justify-between items-center z-50">
		<!-- Logo start -->
		<div class="h-full flex flex-col justify-center">
			<p class="tracking-widest font-semibold text-teal-900">Jeff's Stow & Go</p>
			<p class="tracking-widest font-light text-teal-900">SELF STORAGE</p>
		</div>
		<!-- Logo end -->

		<!-- Toggler start -->
		<button role="menubar" class="md:hidden" @click="navToggle()">
			<i class="fa-solid fa-bars text-2xl"></i>
		</button>
		<!-- Toggler end -->

		<!-- Menu content start -->
		<div class="absolute left-0 right-0 translate-y-16 bg-opacity-90 bg-white md:bg-none md:bg-opacity-0 shadow hidden md:flex flex-col gap-4 items-center p-4 md:flex-row md:static md:shadow-none md:translate-y-0" role="menu" aria-expanded="false">
			<!-- Links start -->
			<a href="#" role="menuitem">
				<p class="mx-4">Home</p>
			</a>

			<a href="#about-section" role="menuitem">
				<p class="mx-4">About</p>
			</a>

			<a href="#services-section" role="menuitem">
				<p class="mx-4">Services</p>
			</a>

			<button class="btn bg-teal-900" role="menuitem" @click="handleContactUsButtonClick">
				Contact us
			</button>
			<!-- Links end -->
		</div>
		<!-- Menu content end -->
	</nav>
    <!-- Navbar end -->
</template>

<script>

export default {
    methods: {
		// Toogle navbar mode 
        navToggle() {
			let menu = document.querySelector("[role='menu']");
			let isExpanded = menu.getAttribute('aria-expanded');
			menu.setAttribute('aria-expanded', !isExpanded);
			menu.classList.toggle('hidden');
			menu.classList.toggle('flex');
		},
		handleContactUsButtonClick() {
			const element = document.getElementById('contact-section');
			if (element) {
				element.scrollIntoView({ behavior: 'smooth' });
			}
		}
	}
}
</script>

<style>

</style>