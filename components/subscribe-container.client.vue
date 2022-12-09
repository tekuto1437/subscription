<template>
    <div class="container">
        <h1 class="container-title">Choose a suitable tariff</h1>
        <div class="tariffs-container">
            <TariffCard  
            v-for="tariff of avalibleTariffs"
            :title=tariff.title 
            :price=tariff.price 
            :isAvalible=tariff.isAvalible 
            :diskSpace=tariff.diskSpace />
        </div>
    </div>
</template>

<script>
export default {
    name: 'Subscribe-container',
    data() {
        return {
            avalibleTariffs: [
                {
                    title: 'Free',
                    price: 0.00,
                    isAvalible: true,
                    diskSpace: '100 Gb'
                },
                {
                    title: 'Lite',
                    price: 6.99,
                    isAvalible: false,
                    diskSpace: '350 Gb'
                },
                {
                    title: 'Pro',
                    price: 12.99,
                    isAvalible: false,
                    diskSpace: '1 TB'
                },
                {
                    title: 'Ultra',
                    price: 20.99,
                    isAvalible: false,
                    diskSpace: '3 TB'
                }
            ]
        }
    }
}

</script>

<style>

.container {
    background-color: #484C54;
    width: 80%;
    height: 80%;
    border-radius: 15px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    padding: 3rem;
}

.container-title {
    width: 100%;
    height: 10%;
    text-align: center;
    color: white;
}

.tariffs-container {
    width: 100%;
    height: 90%;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    place-items: center;
}
</style>