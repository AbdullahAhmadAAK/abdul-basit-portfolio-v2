<script>
  let boxes = [
    {
      title: "THE PERSON",
      description:
        "Abdul Basit Pawar is a renowned mathematics tutor for preparation of GRE (Quan), SAT (Math section) and undergraduate math courses. Born on August 06, 2002, in Gujranwala, he has become a top-rated tutor both among local and international students. His journey to success is marked by perseverance, passion, and a deep understanding of mathematics.",
    },
    {
      title: "THE JOURNEY",
      description:
        "Abdul Basit's journey is a unique one, taking him from the world of entrepreneurship to help students as a tutor. He is the Co-founder of bikechaiye.com, the pioneering fuel bike rental service for university students and Yodobikes.com, the only electric scooter sharing service in Pakistan. Despite achieving entrepreneurial acclaim initially, Abdul Basit felt a calling to pursue a path that allowed him to help students.",
    },
    {
      title: "THE TRANSITION",
      description:
        "AbdulBasit's transition from entrepreneur to math tutor stemmed from a desire to devote himself for mathematics. He began by assisting more than a thousand students at LUMS Math Circles, drawing on his own experiences and challenges to connect with students. He then started working as a private tutor for mathematics and enjoying it till today. His relatable approach and simple language made him students’ favourite.",
    },
  ];
</script>

<section id="about" class="about mb-16 mt-4">
  <h3 class="text-center h-10 font-extrabold text-[34px] text-[#080808]">
    About
  </h3>
  <div class="about-container flex flex-col px-32 mt-10">
    <div class="flex gap-8">
      <div
        class="border border-[#ddd] rounded-lg shadow-md flex-1 overflow-hidden"
      >
        <img src="/about-1.jpg" alt="About 1" />
      </div>
      <div
        class="border border-[#ddd] rounded-lg shadow-md flex-1 overflow-hidden"
      >
        <img src="/about-2.jpg" alt="About 2" />
      </div>
      <div
        class="border border-[#ddd] rounded-lg shadow-md flex-1 overflow-hidden"
      >
        <img src="/about-3.jpg" alt="About 3" />
      </div>
    </div>
    <div class="flex gap-8">
      {#each boxes as box}
        <div
          class="bg-[#ebf5ff] border border-1 text-center shadow-md flex flex-col gap-4 flex-1 border-[#ddd] rounded-lg p-5"
        >
          <h3 class="font-extrabold text-[30px] text-[#080808]">
            {box.title}
          </h3>
          <p
            class=" font-medium text-[14px] leading-[24px] tracking-[1%] content-center text-[#080808]"
          >
            {box.description}
          </p>
        </div>
      {/each}
    </div>
  </div>
</section>
