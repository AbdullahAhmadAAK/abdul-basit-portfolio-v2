<script>
  import { sectionHorizontalPadding } from "../../lib/styles";
  const works = [
    {
      title:
        "An Empirical Analysis of Amazon Product Sales: A Comprehensive Study on the Applicability of Zipf’s Law",
      supervisor:
        "<a href='https://lums.edu.pk/lums_employee/993' target='_blank' class='text-blue-500 hover:text-blue-700 underline'>Dr. Sultan Sial</a>, Associate Professor",
      knowMoreLink: "https://sbasse.lums.edu.pk/applying-math-in-real-world",
      image: "abdul-basit-presentation-research-1.png",
      alt: "Abdul Basit Pawar giving a presentation for a research paper on Applicability of Zipf's Law",
    },
    {
      title:
        'Verification of Study: "Impact of School Closures and Reopening on Covid-19 Caseload in 6 Cities of Pakistan"',
      supervisor:
        "<a href='https://lums.edu.pk/lums_employee/993' target='_blank' class='text-blue-500 hover:text-blue-700 underline'>Dr. Sultan Sial</a>, Associate Professor",
      knowMoreLink:
        "https://journals.plos.org/globalpublichealth/article?id=10.1371/journal.pgph.0000648",
      image: "corona-research.jpg",
      alt: "Placeholder for random research papers",
    },
  ];
</script>

<section class="text-center mx-auto {sectionHorizontalPadding} my-10">
  <div class="mb-12">
    <h4 class="font-extrabold text-[34px] md:text-[40px]">
      Research Experience
    </h4>
  </div>

  <div class="flex gap-16 justify-center flex-wrap">
    {#each works as work}
      <div class="flex flex-col items-center gap-4 w-full max-w-[300px]">
        <div class="w-full h-[200px] overflow-hidden rounded-lg shadow-lg">
          <img
            src={work.image}
            alt={work.alt}
            class="w-full h-full object-cover"
          />
        </div>
        <h4
          class="font-extrabold text-[18px] md:text-[22px] text-[#080808] leading-tight"
        >
          {work.title}
        </h4>
        <p
          class="text-[#9C9C9C] font-normal text-[12px] md:text-[14px] leading-[20px] md:leading-[24px]"
        >
          Supervised by: {@html work.supervisor}
        </p>
        <a href={work.knowMoreLink} target="_blank" rel="noopener noreferrer">
          <button
            class="py-2 px-8 md:py-3 md:px-10 text-white bg-[#3F8E00] hover:bg-[#2F6B00] rounded-md font-bold text-[14px] md:text-[16px] mt-4 transition-shadow border-[#62BA1B] border-2 box"
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
