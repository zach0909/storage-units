<template>
	<!-- Navbar start -->
	<navbar-element></navbar-element>
	<!-- Navbar end -->

	<!-- Rendered view start -->
	<home-view></home-view>
	<!-- Rendered view end -->

</template>

<script>
import NavbarElement from '@/components/NavbarElement.vue';
import HomeView from '@/HomeView.vue';

export default {
	components: {
		HomeView,
		NavbarElement
	}
}
</script>

<style>

</style>
