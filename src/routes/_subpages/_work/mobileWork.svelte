<script>
  import { content } from "./content.js"
</script>

<div class="h-full w-full overflow-scroll">
  <div class="sticky top-20 grid align-center background-white ">
    <p class="pl-2 text-5xl lg:text-8xl text-center all-round-gothic-medium-oblique uppercase spacing ">
      WORK
    </p>
  </div>
  <div class="h-fit w-full mt-28 pb-8 grid place-items-center all-round-gothic-xlig-oblique overflow-scroll join join-vertical">
    {#each Object.entries(content) as [key, value]}
       <!-- content here -->
       <div class="collapse collapse-plus join-item">
        <input type="radio" name="my-accordion-3" />
        <div class="collapse-title uppercase text-3xl min-h-0 leading-4">
          {key}
        </div>
        <div class="collapse-content text-sm overflow-scroll">
          <!-- svelte-ignore a11y-missing-attribute -->
            <iframe
							src={value.video}
							frameborder="0"
							allow="autoplay;"
							allowfullscreen
							class="w-full p-0 m-0 py-4 "
						/>
          <p>{value.text}</p>
        </div>
      </div>
    {/each}
  </div>
</div>
