<script lang="ts" context="module">
    let sequence = 0
</script>
<script lang="ts">
    const id = `Check_${sequence++}`;
    export let checked = false
    export let label = "チェック"
</script>

<input {id} type="checkbox" bind:checked/><label for={id}>{label}</label>

<style lang="scss">
    input {
        appearance: none;
        &:checked+label {
            background-color: gold;
        }
        &:focus+label {
            border: 1px dotted red;
        }
    }
    label {
        border: 1px solid transparent;
        display: inline-block;
        padding: 0.5em 2em;
        &:hover {
            background-color: goldenrod;
        }
        user-select: none;
    }
</style>