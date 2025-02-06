<script setup>
import { ref } from 'vue';1

const numero = ref(0);

function aumentar(){
    if(numero.value < 4){
        numero.value ++
    }
}

function diminuir(){
    if(numero.value > 0){
        numero.value --
    }
}
</script>

<template>
    <header>
        <nav>
            <h1>Comprei</h1>
            <ul>
               <a href="http://"><li>Inicio</li></a> 
               <a href="http://"><li>Produtos</li></a> 
               <a href="http://"><li>Carrinho</li></a> 
            </ul>
        </nav>
    </header>
    <main>
        
        <section>
            <div>
                <img :src= "'https://static.netshoes.com.br/produtos/bicicleta-aro-29-dropp-aluminum-21-marchas-freio-a-disco-suspensao-dianteira/02/JWY-0062-002/JWY-0062-002_zoom2.jpg?ts=1582053196&'" alt="Bicicleta">
            </div>
            <div class="info">
                <div class="descricao">
                    <h3>Bicicleta</h3>
                    <span> <i class="fa-solid fa-star"></i> 4.9  |  2.2 mil avaliações</span>
                    <h4>R$ 800,00</h4>
                </div>
                <div class="contador">
                    
                    <button @click="diminuir">-</button>
                    <h2>{{ numero }}</h2>
                    <button @click="aumentar">+</button>
                </div>
                <div class="botoes">
                    <button @click=""  class="button1">Adicionar ao Carrinho</button>
                    <button @click="">Comprar</button>
                </div>
            </div>
        </section>
    </main>
    
</template>

<style scoped lang="scss" >

      
nav{
        background-color: orangered;
        display: flex;
        justify-content: space-around;
        align-items: center;
        width: 99vw;
        height: 8vh;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        color: #ffff;
}


ul{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 30vw;

    a{
        text-decoration: none;
    }

    li{
        list-style: none;
        color: #ffff;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 15px;
        font-weight: 50;
    }
}

main{
    background-color: rgb(236, 233, 233);
    height: 92vh;
    width: 99vw;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

section{
    height: 82vh;
    width: 70vw;
    background-color: #ffff;
    display: flex;
    justify-content: center;
    align-items: center;
}

img{
    height: 50vh;
}

.info{
    height: 60vh;
    width: 30vw;
    margin-left: 65px;
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    flex-direction: column;
}

.descricao{
    height: 25vh;
    width: 20vw;
    display: flex;
    align-items: baseline;
    flex-direction: column;

    h3{
        font-size: 30px;
        font-weight: 50;
    }

    i{
        font-size: 10px;
    }

    span{
        font-size: 14px;
        margin-top: 5px;
        font-weight: 25;
        text-decoration: none;
    }

    h4{
        margin-top: 50px;
        font-size: 30px;
        font-weight: 600;
        color: orangered;
    }
}

.contador{
    height: 5vh;
    width: 7vw;
    display: flex;
    justify-content: space-between;

    button{
        width: 30px;
        color: orangered;
        font-size: 20px;
        border: none;
    }

    h2{
        font-weight: 400;
    }
}

.botoes{
    height: 9vh;
    width: 32vw;
    display: flex;
    justify-content: space-between;

    .button1{
        height: 7vh;
        width: 15vw;
        border: solid 1px orangered;
        background-color: hsl(16, 100%, 50%, 0.2);
        color: orangered;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 15px;

        &:hover{
            cursor: pointer;
        }
    }

    button{
        height: 7vh;
        width: 15vw;
        background-color: orangered;
        border: none;
        color: #ffff;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 15px;

        &:hover{
            cursor: pointer;
        }
    }
}
</style>
