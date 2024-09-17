<script>
  const works = [
    {
      title: "An Empirical Analysis of Amazon Product Sales: A Comprehensive Study on the Applicability of Zipf’s Law",
      supervisor: "Dr. Sultan Sial, Associate Professor",
      knowMoreLink: "https://sbasse.lums.edu.pk/applying-math-in-real-world",
      image: "zipfs-law-research.png",
    },
    {
      title: 'Verification of Study: "Impact of School Closures and Reopening on Covid-19 Caseload in 6 Cities of Pakistan"',
      supervisor: "Dr. Sultan Sial, Associate Professor",
      knowMoreLink: "https://journals.plos.org/globalpublichealth/article?id=10.1371/journal.pgph.0000648",
      image: "corona-research.jpg",
    },
  ];
</script>

<section class="text-center mx-auto px-32 my-10">
  <div class="mb-12">
    <h4 class="font-extrabold text-[34px]">Research Experience</h4>
  </div>

  <div class="flex gap-16 justify-center flex-wrap">
    {#each works as work}
      <div class="flex flex-col items-center gap-4 w-[300px]">
        <div class="w-full h-[200px] overflow-hidden rounded-lg shadow-lg">
          <img src={work.image} alt={work.title} class="w-full h-full object-cover" />
        </div>
        <h4 class="font-extrabold text-[22px] text-[#080808] leading-tight">{work.title}</h4>
        <p class="text-[#9C9C9C] font-normal text-[14px] leading-[24px]">
          Supervised by: {work.supervisor}
        </p>
        <a href={work.knowMoreLink} target="_blank" rel="noopener noreferrer">
          <button
            class="py-3 px-10 text-white bg-[#3F8E00] hover:bg-[#2F6B00] rounded-md font-bold text-[16px] mt-4 transition-shadow border-[#62BA1B] border-2 box"
          >
            Know More &gt;
          </button>
        </a>
      </div>
    {/each}
  </div>
</section>

<style>
  .box {
    box-shadow: 0px 8px 20px rgba(63, 142, 0, 0.3);
  }
</style>
