<script>
  import SocialIcons from "@rodneylab/svelte-social-icons"; // Import the SocialIcons component

// Links for the footer
const links = [
  { name: "Home", href: "#home" },
  { name: "About", href: "#about" },
  { name: "Qualifications", href: "#qualification" },
  { name: "Study Plans", href: "#study-plans" },
];

// Social media icon data for SocialIcons component
const socialIcons = [
  { name: "Facebook", href: "https://www.facebook.com/profile.php?id=100071005491576", network: "facebook" },
  { name: "LinkedIn", href: "https://www.linkedin.com/in/abdulbasitpawar/", network: "linkedin" },
  { name: "YouTube", href: "https://www.youtube.com/@AbdulBasitpawarmath", network: "youtube" },
  { name: "WhatsApp", href: "https://wa.me/message/CASFE6CD3FVQI1", network: "whatsapp" },
];
</script>

<footer class="bg-black text-white py-10">
  <div
    class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-start"
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
    <div class="text-left mb-6 md:mb-0"> <!-- Align left instead of center -->
      <h2 class="text-xl font-semibold mb-4">Socials</h2>
      <div class="flex space-x-4">
        {#each socialIcons as social}
          <a href={social.href} target="_blank" class="hover:text-gray-400">
            <SocialIcons alt={social.name} network={social.network} />
          </a>
        {/each}
        <a href="mailto:pa@abdulbasitpawar.com" target="_blank">
          <SocialIcons alt="email" network="email" /> <!-- Email icon component -->
        </a>
      </div>
    </div>
  </div>
</footer>
