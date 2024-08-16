<script>
  import SectionWrapper from "./SectionWrapper.svelte";
  import ProductCard from "./ProductCard.svelte";

  let productFeatures = [
    {
      featureList: [
        "Daily streak counter",
        "Weights and reps tracker",
        "Community challenges",
        "Every workout is new and exciting",
      ],
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, aut unde doloremque fugit facilis soluta fugiat officiis provident adipisci similique",
      imgUrl: "https://m.media-amazon.com/images/I/71nu-2agGOL._SX342_.jpg",
    },
    {
      featureList: [
        "Daily streak counter",
        "Weights and reps tracker",
        "Community challenges",
        "Every workout is new and exciting",
      ],
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, aut unde doloremque fugit facilis soluta fugiat officiis provident adipisci similique",
      imgUrl:
        "https://m.media-amazon.com/images/I/510HBJu6A0L._SX300_SY300_QL70_FMwebp_.jpg",
    },
    {
      featureList: [
        "Daily streak counter",
        "Weights and reps tracker",
        "Community challenges",
        "Every workout is new and exciting",
      ],
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, aut unde doloremque fugit facilis soluta fugiat officiis provident adipisci similique",
      imgUrl: "https://m.media-amazon.com/images/I/51Z830F+LRL._SY300_.jpg",
    },
  ];
</script>

?
<SectionWrapper id="product">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Start your lifetime <span class="text-indigo-400">gym streak</span> today
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Features For Everyone
      </h3>
    </div>
    {#each productFeatures as productFeature, index}
      <ProductCard {productFeature} {index}>
        {#if index === 0}
          Experience a beginner exercise <span class="text-indigo-400"
            >master</span
          > class
        {:else if index === 1}
          Lay the foundation for <span class="text-indigo-400 font-medium"
            >routine</span
          >and consistency
        {:else}
          Workout specific to your <span class="text-indigo font-medium"
            >enviornment</span
          >
          and <span class="text-indigo font-medium">experties</span>
        {/if}
      </ProductCard>
    {/each}
  </div>
</SectionWrapper>
