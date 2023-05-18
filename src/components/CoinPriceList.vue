
<template>
    <div>
        <div class="grid">
<!--            <div class="col">-->
<!--                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><g fill="none" class="nc-icon-wrapper"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21 12 17.27z" fill="#848e9c"></path></g></svg>-->

<!--            </div>-->
            <div class="col">
                <ul>
                    <li v-for="(pair, index) in pairNames" class="inline text-gray-300 mx-1">
                        {{ pair }}
                    </li>
                </ul>
            </div>
        </div>

        <div class="border border-slate-500 px-5 pt-5">
            <table class="table-auto  w-full text-left">
                <thead>
                <tr>
                    <th>Pair</th>
                    <th>Price</th>
                    <th class="text-right">Change</th>
                </tr>
                </thead>
                <tbody>
                <tr v-for="item in pairPrices">
                    <td>
                        <span>
                            {{ item.pair.substring(0, item.pair.indexOf('/')) }}
                        </span>
                        /
                       <span class="text-gray-400">
                            {{ item.pair.substring(item.pair.indexOf('/') + 1) }}
                       </span>
                    </td>
                    <td :class="{ 'text-red-600': item.change.startsWith('-'), 'text-green-300': item.change.startsWith('+') }">{{ item.price }}</td>
                    <td class=" text-right" :class="{ 'text-red-600': item.change.startsWith('-'), 'text-green-300': item.change.startsWith('+') }">{{ item.change }}</td>
                </tr>
                </tbody>
            </table>
        </div>




        <div class="border border-slate-500 px-5 pt-5">
            <div class="font-bold text-yellow-300">Market Trades</div>
            <table class="table-auto  w-full text-left">
                <thead>
                <tr>
                    <th>Price (USDT)</th>
                    <th>Amount (BTC)</th>
                    <th class="text-right">Time</th>
                </tr>
                </thead>
                <tbody>
                <tr v-for="item in marketTrades">
                    <td class="text-green-300">{{ item.price }}</td>
                    <td class="text-gray-400">{{ item.amount }}</td>
                    <td class="text-gray-400 text-right">{{ item.time }}</td>
                </tr>
                </tbody>
            </table>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)

const pairNames = ref([
    'Margin',
    'USDT',
    'TUSD',
    'BUSD',
    'BNB',
    'BTC',
    'ALTS',
    'FIAT',
    'Zones',
]);

const pairPrices = ref([
        {
            pair: "1INCH/BTC3x",
            price: 0.00001494,
            change: "-3.11%"
        },
        {
            pair: "AAVE/BTC3x",
            price: 0.002410,
            change: "+3.34%"
        },
        {
            pair: "ACA/BTC",
            price: 0.00000209,
            change: "-1.42%"
        },
        {
            pair: "ACH/BTC",
            price: 0.00000101,
            change: "+2.02%"
        },
        {
            pair: "ADA/BTC3x",
            price: 0.00001369,
            change: "+0.15%"
        },
        {
            pair: "ADX/BTC",
            price: 0.00000595,
            change: "-2.46%"
        },
        {
            pair: "AERGO/BTC3x",
            price: 0.00000417,
            change: "+0.24%"
        },
        {
            pair: "AGIX/BTC3x",
            price: 0.00000967,
            change: "+0.21%"
        },
        {
            pair: "AGLD/BTC3x",
            price: 0.00001460,
            change: "-1.88%"
        },
        {
            pair: "ALCX/BTC",
            price: 0.000662,
            change: "-4.75%"
        },
        {
            pair: "ALGO/BTC3x",
            price: 0.00000621,
            change: "-1.27%"
        },
        {
            pair: "ALICE/BTC3x",
            price: 0.0000484,
            change: "-1.22%"
        },
        {
            pair: "ALPACA/BTC3x",
            price: 0.00000773,
            change: "-1.40%"
        }
    ]
);

const marketTrades = ref([
        {
            "price": "27,384.37",
            "amount": "0.00200",
            "time": "13:38:36"
        },
        {
            "price": "27,384.37",
            "amount": "0.00105",
            "time": "13:38:36"
        },
        {
            "price": "27,384.38",
            "amount": "0.00174",
            "time": "13:38:35"
        },
        {
            "price": "27,384.38",
            "amount": "0.02391",
            "time": "13:38:35"
        },
        {
            "price": "27,384.38",
            "amount": "0.00157",
            "time": "13:38:34"
        },
        {
            "price": "27,384.38",
            "amount": "0.00095",
            "time": "13:38:33"
        },
        {
            "price": "27,384.37",
            "amount": "0.00336",
            "time": "13:38:33"
        },
        {
            "price": "27,384.38",
            "amount": "0.06656",
            "time": "13:38:33"
        },
        {
            "price": "27,384.38",
            "amount": "0.00036",
            "time": "13:38:32"
        },
        {
            "price": "27,384.37",
            "amount": "0.00195",
            "time": "13:38:32"
        },
        {
            "price": "27,384.37",
            "amount": "0.00144",
            "time": "13:38:32"
        },
        {
            "price": "27,384.37",
            "amount": "0.00177",
            "time": "13:38:32"
        },
        {
            "price": "27,384.37",
            "amount": "0.00196",
            "time": "13:38:30"
        },
        {
            "price": "27,384.38",
            "amount": "0.44286",
            "time": "13:38:30"
        },
        {
            "price": "27,384.37",
            "amount": "0.02870",
            "time": "13:38:30"
        },
        {
            "price": "27,384.38",
            "amount": "0.00479",
            "time": "13:38:30"
        },
        {
            "price": "27,384.37",
            "amount": "0.00544",
            "time": "13:38:29"
        },
        {
            "price": "27,384.38",
            "amount": "0.00749",
            "time": "13:38:29"
        }
    ]
)

</script>


<style scoped>
</style>
