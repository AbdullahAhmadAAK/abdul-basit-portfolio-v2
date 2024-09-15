<script>
  let boxes = [
    {
      title: 'Foundation',
      features: [
        '4 sessions per week',
        'Practice material'
      ],
      internationalPrice: 'USD 250/month',
      subcontinentalPrice: 'PKR 30,000/month'
    },
    {
      title: 'Mastery',
      features: [
        '6 sessions per week',
        'Practice material',
        'Mock tests',
        'WhatsApp support'
      ],
      internationalPrice: 'USD 325/month',
      subcontinentalPrice: 'PKR 40,000/month'
    }
  ]


  let isSubcontinentToggled = true

  const toggleInternationalStudents = () => {
    isSubcontinentToggled = false
  }

  const toggleSubcontinentStudents = () => {
    isSubcontinentToggled = true
  }
</script>

<section id="study-plans" class="study-plans bg-[#080808] px-32 py-16">
  

  <h2 class="text-white text-center">Study Plans</h2>

  <div class="flex justify-center gap-2 bg-gray-500 w-fit mx-auto text-white my-4 p-1 rounded-md">
    <button 
      class="{isSubcontinentToggled ? 'bg-green-400' : 'bg-gray-400 hover:bg-green-300'} rounded-md px-2" 
      on:click={toggleSubcontinentStudents}
    >
      Indian Subcontinent Students
    </button>
    <button 
      class="{!isSubcontinentToggled ? 'bg-green-400' : 'bg-gray-400 hover:bg-green-300'} rounded-md px-2" 
      on:click={toggleInternationalStudents}
    >
      International Students
    </button>
  </div>

  <div class="study-plans-container flex justify-between">

    {#each boxes as box}
      <div class="flex flex-col gap-2 bg-white rounded-xl shadow-md p-[20px] w-[45%]">
        <div class="flex justify-between">
          <h4>{box.title}</h4>
          <h4>{isSubcontinentToggled ? box.subcontinentalPrice : box.internationalPrice}</h4>
        </div>
        
        <hr>

        {#each box.features as feature}
          <p>
            <span class="checkmark">✔</span>{feature}
          </p>
        {/each}
      </div>
    {/each}
   
  </div>

  <p class="text-center text-white">
    Prices last updated on 1st September 2024. For the latest prices, please consult us at this WhatsApp number: +92-3314160816.
  </p>
</section>