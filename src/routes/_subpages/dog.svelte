<script>
	import Sidebar from "../sidebar.svelte"
    let wink = false;
    let src = "SVG_DOGS/Asset 4.svg"
</script>

<div class="wink h-full w-full z-50 bg-white">
    <img class="w-4/12" alt="logo" {src} on:mouseenter={() => {
        console.log("enter");
            src="SVG_DOGS/Asset 5.svg"
    }}
    on:mouseleave={() => {
        console.log("leave");
            src="SVG_DOGS/Asset 4.svg"
    }}
    on:click={()=>{
        // CHANGE SRC TO ASSET 5 FOR 1 SECOND
        src="SVG_DOGS/Asset 5.svg"
        setTimeout(() => {
            src="SVG_DOGS/Asset 4.svg";
        }, 1000);
    }}
    >
</div>

<style lang="postcss">
    .wink{
        @apply w-full h-full grid grid-cols-1 place-items-center;
    }
</style>