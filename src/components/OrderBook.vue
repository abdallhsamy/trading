
<template>
<div class="text-sm">

    <div class="border border-slate-500">
        <table class="table-auto mx-5 my-1">
            <thead>
            <tr>
                <th>Price(USDT)</th>
                <th>Amount(BTC)</th>
                <th class="text-right">Total</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="item in sellItems">
                <td class="text-red-700">{{ item.price }}</td>
                <td class="text-gray-300">{{ item.amount }}</td>
                <td class="text-gray-300 text-right">{{ item.total }}</td>
            </tr>
            </tbody>
        </table>
    </div>

    <div class="border border-slate-500	 ">
    <table class="table-auto mx-5 my-1">
        <thead>
        <tr>
            <th >27400.01</th>
            <th>27.40001</th>
            <th class="text-right">More</th>
        </tr>
        </thead>
        <tbody>
        <tr v-for="item in buyItems">
            <td class="col text-red-700">{{ item.price }}</td>
            <td class="col text-gray-300">{{ item.amount }}</td>
            <td class="col text-gray-300 text-right">{{ item.total }}</td>
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

const sellItems = ref([
  {
    "price": 27365.02,
    "amount": 0.00069,
    "total": 18.88186
  },
  {
    "price": 27365.00,
    "amount": 0.00050,
    "total": 13.68250
  },
  {
    "price": 27364.89,
    "amount": 0.00134,
    "total": 36.66895
  },
  {
    "price": 27364.82,
    "amount": 0.00066,
    "total": 18.06078
  },
  {
    "price": 27364.65,
    "amount": 0.00069,
    "total": 18.88161
  },
  {
    "price": 27364.53,
    "amount": 0.00092,
    "total": 25.17537
  },
  {
    "price": 27364.52,
    "amount": 0.16493,
    "total": 4513.23028
  },
  {
    "price": 27364.49,
    "amount": 0.00037,
    "total": 10.12486
  },
  {
    "price": 27364.48,
    "amount": 0.29234,
    "total": 7999.73208
  },
  {
    "price": 27364.47,
    "amount": 0.29234,
    "total": 7999.72916
  },
  {
    "price": 27364.41,
    "amount": 0.14617,
    "total": 3999.85581
  },
  {
    "price": 27364.40,
    "amount": 0.29234,
    "total": 7999.70870
  },
  {
    "price": 27364.33,
    "amount": 0.00690,
    "total": 188.81388
  },
  {
    "price": 27364.30,
    "amount": 0.00132,
    "total": 36.12088
  },
  {
    "price": 27364.28,
    "amount": 0.00069,
    "total": 18.88135
  },
  {
    "price": 27364.18,
    "amount": 0.00366,
    "total": 100.15290
  },
  {
    "price": 27364.15,
    "amount": 0.00099,
    "total": 27.09051
  },
  {
    "price": 27364.14,
    "amount": 0.10740,
    "total": 2938.90864
  },
  {
    "price": 27364.13,
    "amount": 2.24494,
    "total": 2938.90864
  }
]
)

const buyItems = ref([
        {
            "price": 27400.00,
            "amount": 20.88434,
            "total": 572230.91600
        },
        {
            "price": 27399.97,
            "amount": 1.03391,
            "total": 28329.10298
        },
        {
            "price": 27399.96,
            "amount": 0.29280,
            "total": 8022.70829
        },
        {
            "price": 27399.74,
            "amount": 0.31716,
            "total": 8690.10154
        },
        {
            "price": 27399.72,
            "amount": 0.91238,
            "total": 24998.95653
        },
        {
            "price": 27399.61,
            "amount": 0.00074,
            "total": 20.27571
        },
        {
            "price": 27399.60,
            "amount": 0.20000,
            "total": 5479.92000
        },
        {
            "price": 27399.14,
            "amount": 0.00066,
            "total": 18.08343
        },
        {
            "price": 27399.05,
            "amount": 0.09711,
            "total": 2660.72175
        },
        {
            "price": 27398.90,
            "amount": 0.01101,
            "total": 301.66189
        },
        {
            "price": 27398.87,
            "amount": 0.32609,
            "total": 8934.49752
        },
        {
            "price": 27398.63,
            "amount": 0.00793,
            "total": 217.27114
        },
        {
            "price": 27398.62,
            "amount": 0.00435,
            "total": 119.18400
        },
        {
            "price": 27398.27,
            "amount": 0.33181,
            "total": 9091.01997
        },
        {
            "price": 27398.26,
            "amount": 0.00037,
            "total": 10.13736
        },
        {
            "price": 27398.20,
            "amount": 0.16055,
            "total": 4398.78101
        },
        {
            "price": 27398.18,
            "amount": 0.20000,
            "total": 5479.63600
        },
        {
            "price": 27398.10,
            "amount": 0.00066,
            "total": 18.08275
        },
        {
            "price": 27398.00,
            "amount": 0.00200,
            "total": 173.03161
        }
    ]
)

</script>


<style scoped>
</style>
