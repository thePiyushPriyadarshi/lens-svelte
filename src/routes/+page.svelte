<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
  import HeroSection from '../components/(home)/HeroSection.svelte';
  import AboutUs from '../components/(home)/AboutUs.svelte';
  import ServiceSection from '../components/(home)/ServiceSection.svelte';
  import MeetTriSection from '../components/(home)/MeetTriSection.svelte';
  import WhyChooseLens from '../components/(home)/whyChooseLens.svelte';
  import OurVisionSection from '../components/(home)/OurVisionSection.svelte';
  import OurBlogs from '../components/(home)/OurBlogs.svelte';
  import ByTheNumbers from '../components/(home)/ByTheNumbers.svelte';
  import Faq from '../components/(home)/Faq.svelte';
  import GetInTouch from '../components/(home)/GetInTouch.svelte';
</script>

<svelte:head>
	<title>LENS</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
<HeroSection/>
<AboutUs/>
<ServiceSection/>
<MeetTriSection/>
<WhyChooseLens/>
<OurVisionSection/>
<OurBlogs/>
<ByTheNumbers/>
<Faq/>
<GetInTouch/>
</section>

 