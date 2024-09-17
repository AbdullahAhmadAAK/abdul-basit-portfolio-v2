<script>
  import HeaderSection from "./sections/HeaderSection.svelte";
  import HeroSection from "./sections/HeroSection.svelte";
  import GridSection from "./sections/GridSection.svelte";
  import QualificationSection from "./sections/QualificationSection.svelte";
  import AboutSection from "./sections/AboutSection.svelte";
  import VideoSection from "./sections/VideoSection.svelte";
  import ResearchSection from "./sections/ResearchSection.svelte";
  import StudyPlanSection from "./sections/StudyPlanSection.svelte";
  import FaqSection from "./sections/FaqSection.svelte";
  import FooterSection from "./sections/FooterSection.svelte";
</script>

<div class="flex flex-col gap-20 bg-[#080808]">
  <HeaderSection/>
  <HeroSection/>
</div>
<VideoSection/>
<AboutSection/>
<GridSection/>
<QualificationSection/>

<ResearchSection/>
<StudyPlanSection/>
<FaqSection/>
<FooterSection/>