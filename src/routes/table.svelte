<script>
    export let value = '';
    let listIp = [
        {id:1, ip: '123.222.1.2', meaning: 'обнаружен', location: 'неизвестно'}
    ]
    function hhd(x) {
        let www= 'не обнаружен'
                listIp.map(ipvalue => {
                    if(x === ipvalue.ip) {
                        www = "обнаружен"
                    }
                })
            return www
            }

    const addIp = () => {
        listIp = listIp.concat([{
            id: Date.now(),
            ip: value,
            meaning: hhd(value),
            location: 'неизвестно'
        }]);
    }
    
</script>


<div class="block-table">
    <h1>настройки</h1>
    <div class="form-table">
        <input type="text" bind:value>
        <button class="start-btn" on:click={addIp}>START</button>
    </div>
    <table border=".5px" cellspacing=0 cellpadding=10>
        <tr>
            <td>IP</td>
            <td>Значение</td>
           <td>индекс</td>
        </tr>
        {#each listIp as ipp}
            <tr>
                <td>{ipp.ip}</td>
                <td>{ipp.meaning}</td>
                <td>{ipp.location}</td>
            </tr>
        {/each}
    </table>
</div>

<style>
    .block-table {
        display: block;
        margin-left: 50%;
        margin-right: 50%;
        margin-top: 50px;
    }

    .form-table {
        display: flex;
        margin-bottom: 60px;
    }
    .start-btn {
        margin-left: 50px;
        background-color: brown;
    }
</style>