<button on:click> <slot /> </button>

<style>
    button {
        font: larger;
        padding: 0.15rem 0.5rem;
        background-color: #1b1a1a;
        border: 1px solid aliceblue;
        cursor: pointer;
        color: white;
    }

    button:hover {
        opacity: 0.8;
    }
</style>
