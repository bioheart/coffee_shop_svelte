<script>
    import "../app.css";
    import Header from "../components/header.svelte"

</script>

<div class="cointainer mx-auto">
    <div class="px-48 xl:px-96">
        <Header/>
        <slot/>
    </div>
</div>