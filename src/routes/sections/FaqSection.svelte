<script>
  import { sectionHorizontalPadding } from "../../lib/styles";
  
  let faqs = [
    {
      question: "Do I need to pay the fees in advance?",
      answer: "Yes, you need to pay the monthly tuition fee after Free Trial/Demo session.",
      isOpen: false,
    },
    {
      question: "Is there any registration fees?",
      answer: "Yes, a registration fee of Rs 5000 or USD 50 also applies unless stated otherwise.",
      isOpen: false,
    },
    {
      question: "Will my scores improve after taking classes?",
      answer: "Score improvement is usually visible in 3-4 months provided that you complete the assignments.",
      isOpen: false,
    },
  ];

  function toggleFAQ(index) {
    faqs = faqs.map((faq, i) => ({
      ...faq,
      isOpen: i === index ? !faq.isOpen : false
    }));
  }
</script>

<section class="{sectionHorizontalPadding} mt-10">
  <h4 class="font-extrabold text-[30px] text-center">
    Frequently Asked Questions
  </h4>

  <div class="mb-10">
    {#each faqs as faq, index}
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <div class="mb-4">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div
          class="flex justify-between items-center bg-white shadow-md p-4 rounded cursor-pointer hover:bg-gray-100 transition"
          on:click={() => toggleFAQ(index)}
        >
          <div class="text-lg font-semibold">{faq.question}</div>
          <div class="text-2xl text-blue-500">{faq.isOpen ? "-" : "+"}</div>
        </div>
        {#if faq.isOpen}
          <div class="p-4 bg-gray-100 rounded-b mt-1 shadow-inner">
            {faq.answer}
          </div>
        {/if}
      </div>
    {/each}
  </div>
</section>
