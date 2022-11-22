<script>
    import Animals from './Animals.svelte';
    import Dogs from './Dogs.svelte';
    import Cats from './Cats.svelte';
    import Rabbits from './Rabbits.svelte';

    const pages = [Animals, Dogs, Cats, Rabbits];
    let page = 0;

    function menu(){
        page = 0;
    }
    function dog(){
        page = 1;
    }
    function cat(){
        page = 2;
    }
    function rabbit(){
        page = 3;
    }

</script>
<svelte:component 
    this={pages[page]}
    />
<button type="button" on:click={() => menu()}>Menu</button>
<button type="button" on:click={() => dog()}>Dogs</button>
<button type="button" on:click={() => cat()}>Cats</button>
<button type="button" on:click={() => rabbit()}>Rabbits</button>