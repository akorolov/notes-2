<script lang="ts">
	import Tiptap from "$lib/Tiptap.svelte";

    let activeEditor: number = 0

    let noteBlocks = ["test1", "test2", "test3"]

</script>


<div class="m-2 flex flex-col gap-2">
    {#each noteBlocks as block, i}
	    <Tiptap content={block} tags={[]} plain_text={block} id={i} on:showControls={() => activeEditor = i} bind:activeEditor={activeEditor} />
    {/each}
</div>