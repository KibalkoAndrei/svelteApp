<script>
    import Table from "./table.svelte";
    
    let element = 1;


    }

</script>

<div class="menu">
    <button on:click={() => element+=1}>
        настройки
    </button>
    
    <button>
        +сеть
    </button>
    <button>
        +сеть
    </button>
    <button>
        .
    </button>
</div>

{#if element%2==0}
<Table></Table>
{/if}

<!-- <Table></Table> -->


<style>
    .menu{
        display: flex;
        flex-direction: column;
        width: 300px;
        border-right: 1px black solid;
        padding-top: 10px;
    }

    button {
        height: 30px;
        background-color: aquamarine;
        cursor: pointer;
    }
</style>


