<script>
    import missingProductImage from "../../assets/missingProductImage.png"
    import {navigate} from "svelte-routing";
    import imagen from "../../assets/imagenes/39418.jpg"

    export let id;
    export let name;
    export let price;
    export let imageUrl = missingProductImage;



    let handleClick = () => {
        navigate(`/products/${id}`)
    }

</script>

<article on:click={handleClick}>
    <img src={imageUrl} alt="product image"/>
    <div>
        <p>{name}</p>
        <p>{price}€</p>
        <button><img src={imagen}></button>
    </div>
</article>

<style>



    button {
        width: 40px;
        height: 40px;
        margin-left:15px;

    }



    article {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        background-color: white;
        width: 290px;
        height: 300px;
        border-radius: 5px;
        cursor: pointer;
        -webkit-box-shadow: -1px 1px 5px 0px #727171;
        -moz-box-shadow: -1px 1px 5px 0px #727171FF;
        box-shadow: -1px 1px 5px 0px #727171FF;
        padding: 1px;
    }

    article:hover {
        transform: translate(2px, 2px);
    }

    img {
        width: 100%;
        height: 70%;
        object-fit: cover;
        overflow: hidden;
    }

    div {
        padding: 15px;
        display: flex;
       justify-content: space-between;
        align-items: center;

    }
</style>

