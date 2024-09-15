<section class="flex flex-col gap-[60px] text-center mx-auto px-32">
  <div class="flex flex-col gap-2">
    <h4>Research Experience</h4>
    <p>Solving user & business problems since last 15+ years.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. </p>
  </div>

  <div class="flex gap-8 justify-center">
    {#each Array(2) as _}
      <div>
        <div class="min-w-40 min-h-20 bg-green-200"></div>
        <h4>Work name here</h4>
        <p>Labore et dolore magna aliqua. sed do eiusmod tempor incididunt ut labore et dolore magna.</p>
        <button>Know more ></button>
      </div>
    {/each}
  </div>
</section>