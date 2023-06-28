<script>
    let showModal = true;
    function closeModal() {showModal = false;}
</script>



    {#if showModal}
        <div class="modal">
            <div>
                <p>¿Está seguro de que desea cancelar el pedido ?</p>
                <button>Confirmar</button>
                <button on:click={closeModal}>Cerrar</button>
            </div>
        </div>
    {/if}


<style>
   .modal {
        width: 400px;
        height: 400px;

        background-color: #353535;
        position: absolute;

        display: flex;
        align-items: center;
        justify-content: center;
        padding: 40px;
        flex-direction: column;
        color: white;
        font-size: 30px;
        text-align: center;
    }
    </style>