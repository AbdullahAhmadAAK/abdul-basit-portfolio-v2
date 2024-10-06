<script>
  import { sectionHorizontalPadding } from "../../lib/styles";
  let boxes = [
    {
      title: "Foundation",
      features: ["4 sessions per week", "Practice material"],
      internationalPrice: "USD 250/month",
      subcontinentalPrice: "PKR 30,000/month",
      image: '/plan-logo-foundation.png'
    },
    {
      title: "Mastery",
      features: [
        "6 sessions per week",
        "Practice material",
        "Mock tests",
        "WhatsApp support",
      ],
      internationalPrice: "USD 325/month",
      subcontinentalPrice: "PKR 40,000/month",
      image: '/plan-logo-mastery.png'
    },
  ];

  let isSubcontinentToggled = true;

  const toggleInternationalStudents = () => {
    isSubcontinentToggled = false;
  };

  const toggleSubcontinentStudents = () => {
    isSubcontinentToggled = true;
  };
</script>

<section id="study-plans" class="study-plans bg-[#080808] {sectionHorizontalPadding} py-8 md:py-16">
  <h2 class="text-white text-center font-extrabold text-[24px] md:text-[30px] mb-4 md:mb-6">Study Plans</h2>

  <!-- Toggle Buttons -->
  <div class="flex justify-center gap-2 bg-gray-500 w-fit mx-auto text-white p-1 rounded-full">
    <button
      class="{isSubcontinentToggled
        ? 'bg-[#3F8E00]'
        : 'bg-gray-400 hover:bg-[#2F6B00]'} rounded-full px-3 py-1 md:px-4 md:py-2 font-extrabold transition-colors duration-300 ease-in-out text-[10px] md:text-[16px]"
      on:click={toggleSubcontinentStudents}
      aria-label="Toggle Subcontinental Students"
    >
      Indian Subcontinent Students
    </button>
    <button
      class="{!isSubcontinentToggled
        ? 'bg-[#3F8E00]'
        : 'bg-gray-400 hover:bg-[#2F6B00]'} rounded-full px-3 py-1 md:px-4 md:py-2 font-extrabold transition-colors duration-300 ease-in-out text-[10px] md:text-[16px]"
      on:click={toggleInternationalStudents}
      aria-label="Toggle International Students"
    >
      International Students
    </button>
  </div>

  <!-- Study Plan Cards -->
  <div class="study-plans-container flex flex-col md:flex-row justify-between gap-6 md:gap-8 mt-6 md:mt-10">
    {#each boxes as box}
      <div class="flex flex-col gap-4 bg-white rounded-xl shadow-lg p-4 md:p-6 w-full md:w-[45%]">
        <div class="mb-4 md:mb-6">
          <img src={box.image} alt="Logo of Abdul Basit Pawar, Math tutor" class="h-16 md:h-24 w-auto mx-auto md:mx-0" />
        </div>

        <div class="flex flex-col md:flex-row justify-between items-center">
          <h4 class="font-extrabold text-[18px] md:text-[22px] text-[#080808]">{box.title}</h4>
          <h4 class="font-extrabold text-[16px] md:text-[22px] text-[#3F8E00]">
            {isSubcontinentToggled
              ? box.subcontinentalPrice
              : box.internationalPrice}
          </h4>
        </div>

        <hr class="border-gray-300 my-4" />

        {#each box.features as feature}
          <p class="font-medium text-[12px] md:text-[14px] leading-[20px] md:leading-[24px] tracking-[1%] flex gap-4 items-center">
            <span class="text-[#3F8E00] font-bold">✔</span>
            <span>{feature}</span>
          </p>
        {/each}
      </div>
    {/each}
  </div>

  <!-- Price Update Notice -->
  <p class="text-center text-white font-normal text-[12px] md:text-[14px] leading-[20px] md:leading-[24px] tracking-[1%] mt-6 md:mt-10">
    Prices last updated on 1st September 2024. <br> For the latest prices, please
    consult us on WhatsApp at: 
    <a href="https://api.whatsapp.com/message/CASFE6CD3FVQI1" target="_blank" class="text-[#62BA1B] underline">
      +92 328 5399335
    </a>.
  </p>
</section>

<style>
  .box {
    box-shadow: 0px 16px 30px rgba(63, 142, 0, 0.2);
  }
</style>
