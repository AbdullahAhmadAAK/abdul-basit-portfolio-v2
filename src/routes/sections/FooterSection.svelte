<script>
  // Dummy links for the footer
  const links = [
    { name: "Home", href: "#home" },
    { name: "About", href: "#about" },
    { name: "Qualifications", href: "#qualification" },
    { name: "Study Plans", href: "#study-plans" },
  ];

  // Dummy social media icons (You can replace these with actual icons)

  // <div class="flex flex-row" style="gap: 20px;">
  //       <a href="https://www.facebook.com/profile.php?id=100071005491576">
  //         <SocialIcons alt="facebook" network="facebook" />
  //       </a>
  //       <a href="https://www.linkedin.com/in/abdulbasitpawar/">
  //         <SocialIcons alt="linkedin" network="linkedin" />
  //       </a>
  //       <a href="https://www.youtube.com/@AbdulBasitpawarmath">
  //         <SocialIcons alt="youtube" network="youtube" />
  //       </a>
  //       <!-- add whatsapp link here -->
  //       <a href="https://wa.me/message/CASFE6CD3FVQI1">
  //         <SocialIcons alt="whatsapp" network="whatsapp" />
  //       </a>

  const socialIcons = [
    { name: "Facebook", href: "#", icon: "🌐" },
    { name: "Twitter", href: "#", icon: "🐦" },
    { name: "Instagram", href: "#", icon: "📷" },
    { name: "LinkedIn", href: "#", icon: "🔗" },
  ];
</script>

<footer class="bg-black text-white py-10">
  <div
    class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-center"
  >
    <!-- Logo Section -->
    <div class="mb-6 md:mb-0">
      <img src="/basit-logo-abp.jpg" alt="Logo" class="h-40 w-auto" />
    </div>

    <!-- Links/Resources Section -->
    <div class="text-left mb-6 md:mb-0">
      <h2 class="text-xl font-semibold mb-4">Links/Resources</h2>
      <ul>
        {#each links as link}
          <li class="mb-2">
            <a href={link.href} class="hover:text-gray-400">{link.name}</a>
          </li>
        {/each}
      </ul>
    </div>

    <!-- Socials Section -->
    <div class="text-center mb-24">
      <h2 class="text-xl font-semibold mb-4">Socials</h2>
      <div class="flex space-x-4">
        {#each socialIcons as social}
          <a href={social.href} class="hover:text-gray-400 text-2xl"
            >{social.icon}</a
          >
        {/each}
      </div>
      <p class="font-normal text-[14px] leading-[24px] tracking-[1%]">
        x@gmail.com
      </p>
    </div>
  </div>
</footer>
