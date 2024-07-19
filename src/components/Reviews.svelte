<script>
  import ReviewCard from "./ReviewCard.svelte";
  import Reviews from "./Reviews.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  import Stars from "./Stars.svelte";

  let lim = true;
  let reviewsList = [
    {
      name: "Zohaib Ali",
      review:
        "sowley molley is more than just a fitness app, its a lifestyle change. it helped me to develop healthy habits and make better choices about my diet and habits. i am incredibly thanful for this app and the positive impact it had on my life",
      features: [
        "Focus on healthy habits",
        "Nutritional guidence",
        "Positive lifestyle impact",
      ],
    },
    {
      name: "Zohaib Ali",
      review:
        "sowley molley is more than just a fitness app, its a lifestyle change. it helped me to develop healthy habits and make better choices about my diet and habits. i am incredibly thanful for this app and the positive impact it had on my life",
      features: [
        "Focus on healthy habits",
        "Nutritional guidence",
        "Positive lifestyle impact",
      ],
    },
    {
      name: "Zohaib Ali",
      review:
        "sowley molley is more than just a fitness app, its a lifestyle change. it helped me to develop healthy habits and make better choices about my diet and habits. i am incredibly thanful for this app and the positive impact it had on my life",
      features: [
        "Focus on healthy habits",
        "Nutritional guidence",
        "Positive lifestyle impact",
      ],
    },
    {
      name: "Zohaib Ali",
      review:
        "sowley molley is more than just a fitness app, its a lifestyle change. it helped me to develop healthy habits and make better choices about my diet and habits. i am incredibly thanful for this app and the positive impact it had on my life",
      features: [
        "Focus on healthy habits",
        "Nutritional guidence",
        "Positive lifestyle impact",
      ],
    },
  ];
</script>

<SectionWrapper id="reviews">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Don't just take our word for it
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        See what
        <span class="text-indigo-400">Others</span> Have To Say
      </h3>
    </div>

    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} left={true} {index} />
        {/each}
      </div>
      <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} {index} />
        {/each}
      </div>
    </div>
    <button on:click={() => (lim = !lim)} class="specialBtn"
      ><p>{lim ? "Show More" : "Show Less"}</p></button
    >
    <div class="flex flex-col gap-10">
      <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
        Trusted by 1,296 Soldiers
      </p>
      <Stars />
    </div>
  </div>
</SectionWrapper>
