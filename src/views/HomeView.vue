<script setup>
import { useCounterStore } from "@/store/counter";
import {storeToRefs} from "pinia";

const useCounter = useCounterStore();
const {increment} = useCounter;
const {count, double} = storeToRefs (useCounter);
</script>

<template>
    <div>
    <h1>Home Counter: {{ count }}</h1>
    <h2>Double: {{ double }}</h2>
    <button @click="increment" align="left">Increment</button>
    </div>
    <div>
    <img src="https://scontent.fcul3-1.fna.fbcdn.net/v/t39.30808-6/307114118_630143391805580_7231260210015882122_n.png?_nc_cat=102&ccb=1-7&_nc_sid=efb6e6&_nc_ohc=OXEd4qPg14gAX8SkeQo&_nc_ht=scontent.fcul3-1.fna&oh=00_AfARrlSpwtWoueRJyDV445hyYXakDHgsfVTeIJ3Z_AT_PQ&oe=65C0C4DC " width="10%" alt="Image Null" align="center" >
    <h1 style="color:#FF0000">By: AstroZ</h1>
</div>

</template>

