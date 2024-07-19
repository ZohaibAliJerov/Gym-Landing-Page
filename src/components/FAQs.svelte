<script>
  import SectionWrapper from "./SectionWrapper.svelte";

  let faqs = [
    {
      question: "What is Svelte?",
      answer:
        "Svelte is a modern JavaScript framework that compiles your application into efficient, vanilla JavaScript at build time. It shifts much of the work to compile-time, resulting in highly optimized code and better performance.",
    },
    {
      question:
        "How is Svelte different from other frameworks like React or Vue?",
      answer:
        "Svelte differs fundamentally in its approach to building web applications. Unlike React or Vue, which rely on runtime libraries to manage components, Svelte compiles components into optimized JavaScript at build time. This approach reduces the amount of code shipped to the client and results in faster rendering and smaller bundle sizes.",
    },
    {
      question: "Is Svelte suitable for large-scale applications?",
      answer:
        "Yes, Svelte is suitable for building large-scale applications. Its compile-time approach ensures that applications remain efficient and performant even as they grow in size. Many companies have successfully adopted Svelte for their complex web projects.",
    },
    {
      question: "How does Svelte handle state management?",
      answer:
        "Svelte has a built-in reactive system that makes managing state straightforward. It uses reactive declarations (`$:`) to automatically update the DOM when state changes. Additionally, Svelte provides stores and context API for more advanced state management needs.",
    },
    {
      question: "Is it easy to learn Svelte?",
      answer:
        "Yes, many developers find Svelte easy to learn due to its simple and intuitive syntax. It has a smaller API surface compared to other frameworks, which makes it quicker to pick up. Svelte's documentation and community resources also contribute to its ease of adoption.",
    },
  ];
</script>

<SectionWrapper id="faqs">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        For all your questions, qualms & queries
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Frequently Asked Questions
      </h3>
    </div>

    <div class="flexx flex-col gap-8 sm:gap-10 md:gap-14 w-full">
      {#each faqs as faq}
        <div
          class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
          ></div>

          <h4 class="text-lg sm:text-xl md:text-2xl pt-2">{faq.question}</h4>
          <p class="pl-2">{faq.answer}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>
