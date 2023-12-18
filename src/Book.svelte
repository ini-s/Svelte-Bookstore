<script>
    export let bookTitle;
    export let bookPrice;
    export let bookDescription;
</script>

<div>
    <h1>{bookTitle}</h1>
    <p>{bookPrice}</p>
    <p>{bookDescription}</p>
</div>

<style>
    div {
        margin: 1rem;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
        padding: 0.15rem 0.5rem;
    }
    h1 {
        font-size: 1.25rem;
        margin: 0.25rem 0;

        color: aqua;
    }
    p {
        margin: 0.25rem 0;
    }
</style>
