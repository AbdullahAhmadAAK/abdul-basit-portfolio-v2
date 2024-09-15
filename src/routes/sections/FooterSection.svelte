<script>
  // Dummy links for the footer
  const links = [
    { name: "About Us", href: "#" },
    { name: "Services", href: "#" },
    { name: "Contact", href: "#" },
    { name: "Privacy Policy", href: "#" }
  ];

  // Dummy social media icons (You can replace these with actual icons)
  const socialIcons = [
    { name: "Facebook", href: "#", icon: "🌐" },
    { name: "Twitter", href: "#", icon: "🐦" },
    { name: "Instagram", href: "#", icon: "📷" },
    { name: "LinkedIn", href: "#", icon: "🔗" }
  ];
</script>

<footer class="bg-black text-white py-10">
  <div class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-center">
    
    <!-- Logo Section -->
    <div class="mb-6 md:mb-0">
      <img src="/basit-logo-abp.jpg" alt="Logo" class="h-12 w-auto" />
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
    <div class="text-center">
      <h2 class="text-xl font-semibold mb-4">Socials</h2>
      <div class="flex space-x-4">
        {#each socialIcons as social}
          <a href={social.href} class="hover:text-gray-400 text-2xl">{social.icon}</a>
        {/each}
      </div>
    </div>
    
  </div>
</footer>
