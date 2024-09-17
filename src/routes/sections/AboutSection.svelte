<script>
  import { sectionHorizontalPadding } from "../../lib/styles";
  import { onMount } from "svelte";

  let boxes = [
    {
      title: "THE PERSON",
      titleMobileView: "THE <br> PERSON",
      image: "/abdul-basit-portrait-1.jpg",
      imageAlt:
        "Abdul Basit Pawar, a math tutor and entrepreneur, portrait number 1",
      description:
        "Abdul Basit Pawar is a renowned mathematics tutor for preparation of GRE (Quan), SAT (Math section) and undergraduate math courses. Born on August 06, 2002, in Gujranwala, he has become a top-rated tutor both among local and international students. His journey to success is marked by perseverance, passion, and a deep understanding of mathematics.",
    },
    {
      title: "THE JOURNEY",
      titleMobileView: "THE <br> JOURNEY",
      image: "/abdul-basit-portrait-2.jpg",
      imageAlt:
        "Abdul Basit Pawar, a math tutor and entrepreneur, portrait number 2",
      description:
        "Abdul Basit's journey is a unique one, taking him from the world of entrepreneurship to help students as a tutor. He is the Co-founder of <a href='https://bikechaiye.com' target='_blank' class='text-blue-600 underline'>bikechaiye.com</a>, the pioneering fuel bike rental service for university students, and <a href='https://yodobikes.com' target='_blank' class='text-blue-600 underline'>yodobikes.com</a>, the only electric scooter sharing service in Pakistan. Despite achieving entrepreneurial acclaim initially, Abdul Basit felt a calling to pursue a path that allowed him to help students.",
    },
    {
      title: "THE TRANSITION",
      titleMobileView: "THE <br> TRANSITION",
      image: "/abdul-basit-portrait-3.jpg",
      imageAlt:
        "Abdul Basit Pawar, a math tutor and entrepreneur, portrait number 3",
      description:
        "Abdul Basit's transition from entrepreneur to math tutor stemmed from a desire to devote himself for mathematics. He began by assisting more than a thousand students at LUMS Math Circles, drawing on his own experiences and challenges to connect with students. He then started working as a private tutor for mathematics and enjoying it till today. His relatable approach and simple language made him students’ favourite.",
    },
  ];

  const cardWidthStyle = 'md:min-w-[400px] md:max-w-[400px] min-w-[240px] max-w-[240px]'
  
  let isSmallScreen = false;

  onMount(() => {
    // Check initial screen size
    checkScreenSize();

    // Add event listener for resizing
    window.addEventListener("resize", checkScreenSize);

    return () => window.removeEventListener("resize", checkScreenSize);
  });

  function checkScreenSize() {
    isSmallScreen = window.innerWidth < 768; // Adjust breakpoint as needed
  }
</script>

<section id="about" class="about mb-16 mt-4">
  <h3 class="text-center h-10 font-extrabold text-[34px] text-[#080808]">
    About
  </h3>

  <div class="flex {sectionHorizontalPadding} mt-10 gap-8 max-w-[100vw] overflow-x-scroll no-scrollbar">
    {#each boxes as box}
      <div
        class="rounded-lg shadow-md flex flex-col flex-1 border border-[#ddd] {cardWidthStyle}"
      >
        <div class="rounded-t-lg overflow-hidden">
          <img src={box.image} alt={box.imageAlt} />
        </div>

        <div
          class="bg-[#ebf5ff] border border-1 text-center shadow-md flex flex-col gap-8 gap-8 flex-1 border-[#ddd] rounded-b-lg p-5"
        >
          {#key isSmallScreen}
            <h3 class="font-extrabold text-[30px] text-[#080808]">
              {@html isSmallScreen ? box.titleMobileView : box.title}
            </h3>
          {/key}
          
          <p
            class=" font-medium text-[14px] leading-[24px] tracking-[1%] content-center text-[#080808]"
          >
            {@html box.description}
          </p>
        </div>
      </div>
    {/each}
  </div>
  <!-- <div class="about-container flex flex-col {sectionHorizontalPadding} mt-10">
    <div class="flex gap-8">
      <div
        class="border border-[#ddd] rounded-t-lg shadow-md flex-1 overflow-hidden"
      >
        <img src="/abdul-basit-portrait-1.jpg" alt="Abdul Basit Pawar, a math tutor and entrepreneur, portrait number 1" />
      </div>
      <div
        class="border border-[#ddd] rounded-t-lg shadow-md flex-1 overflow-hidden"
      >
        <img src="/abdul-basit-portrait-2.jpg" alt="Abdul Basit Pawar, a math tutor and entrepreneur, portrait number 2" />
      </div>
      <div
        class="border border-[#ddd] rounded-t-lg shadow-md flex-1 overflow-hidden"
      >
        <img src="/abdul-basit-portrait-3.jpg" alt="Abdul Basit Pawar, a math tutor and entrepreneur, portrait number 3" />
      </div>
    </div>
    <div class="flex gap-8">
      {#each boxes as box}
        <div
          class="bg-[#ebf5ff] border border-1 text-center shadow-md flex flex-col gap-4 flex-1 border-[#ddd] rounded-b-lg p-5"
        >
          <h3 class="font-extrabold text-[30px] text-[#080808]">
            {box.title}
          </h3>
          <p
            class=" font-medium text-[14px] leading-[24px] tracking-[1%] content-center text-[#080808]"
          >
            {@html box.description}
          </p>
        </div>
      {/each}
    </div>
  </div> -->
</section>
