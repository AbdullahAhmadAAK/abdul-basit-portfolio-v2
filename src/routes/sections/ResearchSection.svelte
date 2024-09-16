<section class="flex flex-col gap-[60px] text-center mx-auto px-32 mt-10">
  <div class="flex flex-col gap-2">
    <h4 class="font-extrabold text-[30px]">Research Experience</h4>
    <p
      class="text-[#9C9C9C] font-normal text-[14px] leading-[24px] tracking-[1%] w-[500px] ml-60"
    >
      Solving user & business problems since last 15+ years.Lorem ipsum dolor
      sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
      labore et dolore magna aliqua.
    </p>
  </div>

  <div class="flex gap-8 justify-center mb-10">
    {#each Array(2) as _}
      <div>
        <div class="w-[200px] h-[200px] bg-green-200 ml-32"></div>
        <h4 class="font-extrabold text-[30px] mt-4">Work name here</h4>
        <p
          class="text-[#9C9C9C] font-normal text-[14px] leading-[24px] tracking-[1%] mt-4"
        >
          Labore et dolore magna aliqua. sed do eiusmod tempor incididunt ut
          labore et dolore magna.
        </p>
        <button
          class="py-6 px-16 text-[#FFFFFF] bg-[#3F8E00] hover:bg-[#2F6B00] w-fit rounded-sm font-bold text-[16px] mt-6 border-[#62BA1B] border-2 box"
          >Know More ></button
        >
      </div>
    {/each}
  </div>
</section>

<style>
  .box {
    box-shadow: 0px 16px 30px #3f8e0080;
  }
</style>
