<template>
	<header class="header">
		<div class="container-fluid flex">
			<h1 class="header-title"><nuxt-link to="/">Parkour<span>Finder</span></nuxt-link></h1>

			<nav class="header-actions">
				<button class="btn btn--icon" :data-tooltip="$t('header.newspot')"><i class="icon-location" aria-hidden="true"></i><div class="sr-only">{{ $t('header.newspot') }}t</div></button>
				<!--
				<button class="btn btn--icon" :data-tooltip="$t('header.search')"><i class="icon-search" aria-hidden="true"></i><div class="sr-only">{{ $t('header.search') }}</div></button>
				-->
				<nuxt-link class="btn btn--icon" to="/about" :data-tooltip="$t('header.about')"><i class="icon-help" aria-hidden="true"></i><div class="sr-only">{{ $t('header.about') }}</div></nuxt-link>
				<nuxt-link class="btn btn--icon" to="/settings" :data-tooltip="$t('header.settings')"><i class="icon-cog" aria-hidden="true"></i><div class="sr-only">{{ $t('header.settings') }}t</div></nuxt-link>
			</nav>
		</div>
	</header>
</template>

<style lang="stylus">
@require '~assets/styles/variables.styl'
@require '~assets/styles/mixins.styl'

.header
	background $color-white
	padding .5rem 0
	box-shadow 0 0 5px $color-shadow
	position relative
	z-index 10

.header-title
	margin 0
	font 400 $font-size-title/1 $font-stack-heading
	color $color-red
	transform rotate(-8deg)

	a
		color inherit
		text-decoration none
		transition .25s ease

		&:hover
			color darken($color-red, 15%)

	span
		display inline-block
		transform translateY(.225em)

.header-actions
	margin-left auto

	.btn
		position relative

</style>
