<script>
  import { sectionHorizontalPadding } from "../../lib/styles";
  import Carousel from "svelte-carousel";
</script>

<section
  id="content-section"
  class="flex flex-col lg:flex-row justify-between bg-white {sectionHorizontalPadding} my-10"
>
  <div class="flex-1 mb-6 lg:mb-0">
    <div class="bg-green-400 h-[200px] lg:h-[300px] w-full lg:w-[400px]">
      <Carousel>
        <video class="h-full w-full rounded-lg" controls>
          <track kind="captions" />
          <source src="vid1.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <video class="h-full w-full rounded-lg" controls>
          <track kind="captions" />
          <source src="vid2.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </Carousel>
    </div>

    <!-- Mission and Vision Section -->
    <div class="flex flex-col gap-4 flex-1 max-w-full lg:max-w-[60%]">
      <h2 class="font-extrabold text-2xl md:text-3xl lg:text-4xl">
        My Mission
      </h2>
      <p class="font-medium text-sm md:text-base lg:text-lg leading-relaxed">
        My mission is to provide a transformative educational experience that
        fosters intellectual curiosity, critical thinking, and innovation. I am
        committed to equipping students with the knowledge, skills, and ethical
        foundations necessary to excel in their chosen fields and to contribute
        positively to society.
      </p>
      <h2 class="font-extrabold text-2xl md:text-3xl lg:text-4xl mt-6">
        My Vision
      </h2>
      <p class="font-medium text-sm md:text-base lg:text-lg leading-relaxed">
        My vision is to be a leading academic institution recognized for
        excellence in education, research, and community engagement. I aspire to
        create a dynamic learning environment that embraces diversity, promotes
        inclusivity, and drives social progress.
      </p>
    </div>
  </div>
</section>
