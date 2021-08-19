<template>
        <div>
                <h2>Home components</h2><hr />
                <h2 v-for="name in names" :key="name">{{ name }}</h2>
                <hr />
                <div v-for="mobile in mobiles" :key="mobile">
                        <h3 v-if="mobile ==='Vivo'">{{ mobile }}</h3>
                </div><hr />
                <h2>Addition : {{ add(2,4,5) }}</h2>
                <h2>Addition : {{ add(12,14,15) }}</h2>
                <h2>Multiply : {{ multiply(10) }}</h2>
                <!-- <h3 v-for="name in fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h3> -->
        </div>
</template>

<script>
export default {
        name: 'Home',
        data() {
                return{
                        names: ['Rakesh','Nagesh','Mayur'],
                        // fullNames: [
                        //         { first: 'Rakesh', last: 'Lonikar'},
                        //         { first: 'Nagesh', last: 'Kore'},
                        //         { first: 'Mayur', last: 'khemkar'},
                        // ],
                        mobiles:['Sumsung','Vivo','Oppo'],
                        baseMultiplier: 10,
                }
        },
        methods: {
                add(a,b,c){
                        return a+b+c
                },
                multiply(num) {
                        return num * this.baseMultiplier
                },
        },
}
</script>