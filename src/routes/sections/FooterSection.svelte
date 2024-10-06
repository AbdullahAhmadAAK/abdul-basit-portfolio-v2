<script>
  import { onMount } from 'svelte';
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
    { name: 'Email', href: 'mailto:pa@abdulbasitpawar.com', network: 'email' }
  ];

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

<footer class="bg-black text-white py-10">
  <div class="max-w-6xl mx-auto px-4 flex flex-col md:flex-row justify-between items-start space-y-6 md:space-y-0">
    
    <!-- Logo Section -->
    <div class="flex-shrink-0 text-center md:text-left mx-auto md:mx-0">
      <img src="/abdul-basit-logo.png" alt="Logo of Abdul Basit Pawar, Math tutor" class="h-32 w-auto mx-auto md:mx-0" />
    </div>

    <!-- Links/Resources Section -->
    <div class="text-center md:text-left mx-auto md:mx-0">
      <h2 class="text-xl font-semibold mb-4">Links/Resources</h2>
      <ul class="space-y-2">
        {#each links as link}
          <li>
            <a href={link.href} class="hover:text-gray-400">{link.name}</a>
          </li>
        {/each}
      </ul>
    </div>

    <!-- Socials Section -->
    <div class="text-center md:text-left mx-auto md:mx-0">
      <h2 class="text-xl font-semibold mb-4">Socials</h2>
      <div class="flex justify-center md:justify-start space-x-4">
        {#each socialIcons as social}
            {#key isSmallScreen}
              <a href={social.href} target="_blank" class="hover:text-gray-400">
                <SocialIcons
                  alt={"Icon for Abdul Basit Pawar's " + social.name + " account"}
                  network={social.network}
                  height={socialIconSize}
                  width={socialIconSize}
                />
              </a>
            {/key}
        {/each}
      </div>
    </div>
  </div>
</footer>
