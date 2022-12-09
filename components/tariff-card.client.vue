<template>
    <div class="card">
        <div class="card-title-container">
            <h1 class="card-title">{{ title }}</h1>
        </div>
        <div class="card-price-container">
            <span> {{ price === 0 ? '0.00' : price }} € </span>
            <p>{{ isAvalible ? 'for month' : '€/month' }}</p>
        </div>
        <div class="description-container">
            {{ diskSpace }} <span> on disk </span>
        </div>
        <button class="buy-button"> {{ isAvalible ? 'Active' : `Buy ${title}` }} </button>
    </div>
</template>

<script>
export default {
    name: 'tariff-card',
    props: {
        title: {
            type: String
        },
        price: {
            type: Number
        },
        isAvalible: {
            type: Boolean
        },
        diskSpace: {
            type: String
        }
    }
}
</script>

<style>
.card {
    background-color: #B2AEAE;
    height: 90%;
    width: 90%;
    border-radius: 15px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    overflow: hidden;
    align-items: center;
}

.card-title-container {
    background-color: #6E6E73;
    width: 100%;
    height: 15%;
    display: flex;
    justify-content: center;
    align-items: flex-end;
}

.card-title {
    color: white;
    margin: 0 0 5px 0;
}

.card-price-container {
    color: #4F5153;
    text-align: center;
    font-size: 35px;
    margin-top: 40px;
}

.card-price-container > p {
    margin: 0;
    font-size: 18px;
}

.description-container {
    color: #4F5153;
    font-size: 20px;
}

.buy-button {
    outline: none;
    border-radius: 10px;
    background-color: #7E3636;
    border: none;
    width: 85%;
    height: 30px;
    margin: 25px;
    color: white;
    font-size: 18px
}
</style>