<script>
  import SocialIcons from "@rodneylab/svelte-social-icons";
  import { sectionHorizontalPadding } from "../../lib/styles";

  import { onMount } from "svelte";

  let isSmallScreen = false;
  let socialIconSize = '24'; // Default size

  onMount(() => {
    // Check initial screen size
    checkScreenSize();

    // Add event listener for resizing
    window.addEventListener('resize', checkScreenSize);
    
    return () => window.removeEventListener('resize', checkScreenSize);
  });

  function checkScreenSize() {
    isSmallScreen = window.innerWidth < 768; // Adjust breakpoint as needed
    socialIconSize = isSmallScreen ? '32' : '48'; // Adjust sizes as needed
  }
</script>

<section id="home" class="py-8 md:py-16 {sectionHorizontalPadding}">
  <div class="container mx-auto">
    <div
      class="flex flex-col-reverse lg:flex-row items-center justify-between gap-8"
    >
      <div class="flex flex-col gap-6 lg:w-1/2">
        <h1
          class="text-white text-3xl md:text-4xl lg:text-5xl font-extrabold leading-tight md:text-left text-center mx-auto md:mx-0"
        >
          Abdul Basit Pawar
        </h1>
        <p
          class="text-gray-400 text-sm md:text-base lg:text-lg leading-relaxed md:text-left text-center mx-auto md:mx-0"
        >
          Bridging Knowledge and Innovation: Expert Mathematics Tutor and
          Visionary Entrepreneur.
        </p>

        <a href="#study-plans" class="w-fit mx-auto md:mx-0">
          <button
            class="box py-4 px-8 text-white bg-[#3F8E00] hover:bg-[#2F6B00] border border-[#3F8E00] rounded-sm font-bold text-sm md:text-base shadow-lg"
          >
            Let's Get Started >
          </button>
        </a>

        {#key isSmallScreen}
          <div class="flex space-x-4 mt-4 mx-auto md:mx-0">
            <a
              href="https://www.facebook.com/profile.php?id=100071005491576"
              target="_blank"
            >
              <SocialIcons
                alt="Icon for Abdul Basit Pawar's Facebook account"
                network="facebook"
                height={socialIconSize}
                width={socialIconSize}
              />
            </a>
            <a
              href="https://www.linkedin.com/in/abdulbasitpawar/"
              target="_blank"
            >
              <SocialIcons
                alt="Icon for Abdul Basit Pawar's LinkedIn account"
                network="linkedin"
                height={socialIconSize}
                width={socialIconSize}
              />
            </a>
            <a
              href="https://www.youtube.com/@AbdulBasitpawarmath"
              target="_blank"
            >
              <SocialIcons
                alt="Icon for Abdul Basit Pawar's YouTube account"
                network="youtube"
                height={socialIconSize}
                width={socialIconSize}
              />
            </a>
            <a href="https://wa.me/message/CASFE6CD3FVQI1" target="_blank">
              <SocialIcons
                alt="Icon for Abdul Basit Pawar's WhatsApp account"
                network="whatsapp"
                height={socialIconSize}
                width={socialIconSize}
              />
            </a>
            <a href="mailto:pa@abdulbasitpawar.com" target="_blank">
              <SocialIcons
                alt="Icon for Abdul Basit Pawar's email"
                network="email"
                height={socialIconSize}
                width={socialIconSize}
              />
            </a>
          </div>
        {/key}
      </div>

      <div class="w-full lg:w-1/2 flex justify-center lg:justify-end">
        <div
          class="overflow-hidden rounded-full w-40 h-40 md:w-52 md:h-52 lg:w-64 lg:h-64"
        >
          <img
            src="/abdul-basit-passport-photo.png"
            alt="Abdul Basit passport size photo with white background"
            class="w-full h-full object-cover"
          />
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .box {
    box-shadow: 0px 30px 30px #3f8e0080;
  }
</style>
