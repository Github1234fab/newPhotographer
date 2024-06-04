<script>
        import Hero from "../Components/Hero.svelte";
import { fade, slide } from 'svelte/transition';

</script>

<main in:fade={{ duration: 2000 }}>
<Hero />
</main>

<style>
    @import './styles.css';
</style>