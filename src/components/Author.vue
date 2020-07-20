<template>
	<div class="author">
	
<!-- <g-image alt="Author image" class="author__image" src="~/assets/images/author.png" width="180" height="180" immediate="true"/> -->

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			Hi There!
		<br>
			How are you? My name is Stephen Ajulu and welcome to my microblog where i share my thoughts, ideas, progress, logic, logs and more.
			<br>
			Who am i? See <a href="https://stephenajulu.com">here</a>

		<p class="author__links">
		<a href="//twitter.com/stephenajulu"><g-image alt="twitter" src="~/assets/images/twitter.png" width="30" immediate="true"/></a>
      		<a href="//dev.to/stephenajulu"><g-image alt="dev" src="~/assets/images/dev.png" width="30" immediate="true"/></a>
                <a href="//instagram.com/stephenajulu"><g-image alt="instagram" src="~/assets/images/instagram.png" width="30" immediate="true"/></a>
       		<!-- <a href="/rss.xml"><g-image alt="rss" src="~/assets/images/rss.png" width="30" immediate="true"/></a> -->
      		<a href="//github.com/stephenajulu"><g-image alt="github" src="~/assets/images/github.png" width="30" immediate="true"/></a>
      		<a href="//linkedin.com/in/stephenajulu"><g-image alt="linkedin" src="~/assets/images/linkedin.png" width="30" immediate="true"/></a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding-bottom: calc(var(--space) / 2);

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		margin: 0 auto;
		font-size: 1.5em;
		max-width: 400px;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
