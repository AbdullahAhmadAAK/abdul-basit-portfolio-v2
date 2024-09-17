<script>
  import SocialIcons from "@rodneylab/svelte-social-icons";
</script>

<section id="home">
  <div class="flex px-32 pb-16">
    <div class="flex flex-col gap-6">
      <h1
        class="text-white w-[426px] h-[52px] font-extrabold text-[44px] leading-[51.66px]"
      >
        Abdul Basit Pawar
      </h1>
      <p
        class="text-[#9C9C9C] w-[70%] h-[72px] font-normal text-[14px] leading-[24px] tracking-[1%]"
      >
        Intro text: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
        do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </p>

      <a href="#study-plans">
        <button
          class="py-6 px-16 text-[#FFFFFF] bg-[#3F8E00] hover:bg-[#2F6B00] w-fit rounded-sm font-bold text-[16px] border-[#62BA1B] border-2 box"
        >
          Let's Get Started >
        </button>
      </a>
      

      <div class="flex flex-row" style="gap: 20px;">
        <a
          href="https://www.facebook.com/profile.php?id=100071005491576"
          target="_blank"
        >
          <SocialIcons alt="facebook" network="facebook" />
        </a>
        <a href="https://www.linkedin.com/in/abdulbasitpawar/" target="_blank">
          <SocialIcons alt="linkedin" network="linkedin" />
        </a>
        <a href="https://www.youtube.com/@AbdulBasitpawarmath" target="_blank">
          <SocialIcons alt="youtube" network="youtube" />
        </a>
        <a href="https://wa.me/message/CASFE6CD3FVQI1" target="_blank">
          <SocialIcons alt="whatsapp" network="whatsapp" />
        </a>
        <a href="mailto:pa@abdulbasitpawar.com" target="_blank">
          <SocialIcons alt="email" network="email" /> <!-- Email icon component -->
        </a>
      </div>
    </div>

    <div class="overflow-hidden rounded-full h-fit">
      <img src="/abdul-basit-pawar-passport-size-picture.png" alt="" />
    </div>
  </div>
</section>

<style>
  .box {
    box-shadow: 0px 30px 30px #3f8e0080;
  }
</style>
