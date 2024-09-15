<script>
  let faqs = [
    { question: "What is SvelteKit?", answer: "SvelteKit is a framework for building web applications.", isOpen: false },
    { question: "How does reactivity work in Svelte?", answer: "Svelte uses reactive assignments to track data changes.", isOpen: false },
    { question: "What is a store in Svelte?", answer: "A store in Svelte is an object that holds a value and allows you to reactively subscribe to it.", isOpen: false }
  ];

  function toggleFAQ(index) {
    faqs[index].isOpen = !faqs[index].isOpen;
  }
</script>

<section class="px-32">
  <h4>Frequently Asked Questions</h4>

  <div class="">
    {#each faqs as faq, index}
      <div class="mb-4">
        <div class="flex justify-between items-center bg-white shadow-md p-4 rounded cursor-pointer hover:bg-gray-100 transition" on:click={() => toggleFAQ(index)}>
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