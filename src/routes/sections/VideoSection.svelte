<!-- TODO: Aaraiz please replace your video code here and make it work -->
<!-- <div class="carousel slide">
  
  <div class="carousel-indicators">
    <button
      type="button"
      data-bs-target=""
      aria-label="Slide 1"
      aria-current="false"
    ></button><button
      type="button"
      data-bs-target=""
      aria-label="Slide 2"
      aria-current="true"
      class="active"
    ></button>
  </div>

  <div class="carousel-inner">
    <div class="carousel-item">
      <a
        href="https://www.youtube.com/embed/VwSFpOGAwKg?si=GmEegiiwDJAJqBv1"
        target="_blank"
        rel="noopener noreferrer"
        ><div class="w-full h-[200px] lg:w-[640px] lg:h-[360px]">
          <video
            src="/video-1.mp4"
            preload="auto"
            controls
            class="w-full h-full object-cover"
          ></video>
        </div></a
      >
    </div>
    <div class="active carousel-item">
      <a
        href="https://www.youtube.com/embed/d8gqXgLzSDk?si=v9Y1p7H9TEAOjYXC"
        target="_blank"
        rel="noopener noreferrer"
        ><div class="w-full h-[200px] lg:w-[640px] lg:h-[360px]">
          <video
            src="/video-2.mp4"
            preload="auto"
            controls
            autoplay
            class="w-full h-full object-cover"
          ></video>
        </div></a
      >
    </div>
  </div>

  <a class="carousel-control-prev" role="button" tabindex="0" href="#"
    ><span aria-hidden="true" class="carousel-control-prev-icon"
    ></span><span class="visually-hidden">Previous</span></a
  ><a class="carousel-control-next" role="button" tabindex="0" href="#"
    ><span aria-hidden="true" class="carousel-control-next-icon"
    ></span><span class="visually-hidden">Next</span></a
  >
  
</div> -->
<!-- Mission and Vision Section -->
<!-- <script>
  import { sectionHorizontalPadding } from "../../lib/styles";
</script>

<section
  id="content-section"
  class="flex flex-col lg:flex-row justify-between bg-white {sectionHorizontalPadding} my-10"
>
  <div class="flex-1 mb-6 lg:mb-0">
    <div class="bg-green-400 h-[200px] lg:h-[300px] w-full lg:w-[400px]"></div>
  </div>

  <div class="flex flex-col gap-4 flex-1 max-w-full lg:max-w-[60%]">
    <h2 class="font-extrabold text-2xl md:text-3xl lg:text-4xl">My Mission</h2>
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
</section> -->

<!-- <script>
  import { sectionHorizontalPadding } from "../../lib/styles";
</script> -->
  
<script>
  import { sectionHorizontalPadding } from "../../lib/styles";
  import { Swiper, SwiperSlide } from 'svelte-swiper';
  import 'swiper/css';
  import 'swiper/css/navigation';
  import 'swiper/css/pagination';

  let videos = [
    'https://www.youtube.com/embed/VwSFpOGAwKg',
    'https://www.youtube.com/embed/d8gqXgLzSDk'
  ];
</script>

<section
  id="content-section"
  class="flex flex-col lg:flex-row justify-between bg-white {sectionHorizontalPadding} my-10"
>
  <div class="flex-1 mb-6 lg:mb-0">
    <!-- Video Slider using Swiper -->
    <Swiper slidesPerView={1} spaceBetween={30} pagination={{ clickable: true }} navigation={true}>
      {#each videos as video (video)}
        <SwiperSlide>
          <div class="w-full h-[200px] lg:w-[640px] lg:h-[360px]">
            <iframe
              width="100%"
              height="100%"
              src={video}
              title="Video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </SwiperSlide>
      {/each}
    </Swiper>
  </div>

  <!-- Mission and Vision Section -->
  <div class="flex flex-col gap-4 flex-1 max-w-full lg:max-w-[60%]">
    <h2 class="font-extrabold text-2xl md:text-3xl lg:text-4xl">My Mission</h2>
    <p class="font-medium text-sm md:text-base lg:text-lg leading-relaxed">
      My mission is to provide a transformative educational experience that fosters intellectual curiosity, critical thinking, and innovation. I am committed to equipping students with the knowledge, skills, and ethical foundations necessary to excel in their chosen fields and to contribute positively to society.
    </p>
    <h2 class="font-extrabold text-2xl md:text-3xl lg:text-4xl mt-6">My Vision</h2>
    <p class="font-medium text-sm md:text-base lg:text-lg leading-relaxed">
      My vision is to be a leading academic institution recognized for excellence in education, research, and community engagement. I aspire to create a dynamic learning environment that embraces diversity, promotes inclusivity, and drives social progress.
    </p>
  </div>
</section>
