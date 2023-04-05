<script>
    export let values = {
        start1: 20,
        start2: 40
    }
    
    function onUpdate() {
        values = values;
    }
    
</script>
<div on:click={onUpdate}>CLICK TO FORCE UPDATE</div>