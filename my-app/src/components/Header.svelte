<script lang="ts">
    import { Button } from "bits-ui";
</script>

<nav class="navbar">
    <h1 class="text-2xl	text-gray-900 decoration-stone-900 decoration-2">Get2Gether</h1>
    <div class="sub-navbar">
        <a href="/" class="text-lg">Let's Meet</a>
        <a href="/about" class="text-lg">About</a>
        <Button.Root class="inline-flex h-12 items-center justify-center rounded-input bg-dark
            px-[21px] text-[15px] font-semibold text-background shadow-mini
            hover:bg-dark/95 active:scale-98 active:transition-all bg-slate-900	text-gray-50"><a href="/login">Login</a>
        </Button.Root>
    </div>
</nav>

<style>
    nav {
        padding: 0.5rem;
        justify-content: space-between;
        align-items: baseline;
    }

    .navbar{
        display: flex;
        flex-direction: row;
    }

    .navbar a:hover{
        color:black;
        text-decoration: underline;
    }
    
    .sub-navbar {
        display: flex;
        flex-direction: row;
        gap: 10px;
    }
</style>