<template>
    <!-- HTML 요소의 동적 값 표시 -->
    <!-- html 요소 안에 중괄호 2번을 사용함으로써 script에 정의된 변수값을 화면에 표시 -->
    <h1>hello world {{ language }}</h1>

    <!-- :value 문법을 사용하면 단방향 데이터 바인딩 -->
    <input type="text" :value="value1"> 
    <!-- v-model 문법을 사용하면 양방향 데이터 바인딩 -->
    <input type="text" v-model="value2">
    <button @click="showValue">변수변경사항확인</button>

    <h2>{{ count }}</h2>
    <button @click="increament">increament1</button>

    <h1>{{ doubleCount }}</h1>



    <br>
    <input type="number" v-model="count2">
    <button @click="increament2">increament2</button>

</template>
<script>
    export default{
        data(){
            return{
                language:"python",
                value1: "python",
                value2: "java",
                count: 0,
                count2: 0
            }
        },
        // computed는 종속된 반응형 데이터가 변경될 때 함수를 다시 실행하여 값을 계산하는 함수
        computed: {
            doubleCount(){
                return this.count * 2;
            }
        },
        methods:{
            showValue(){
                alert(this.value2);
            },
            increament(){
                this.count++;
            },
            increament2(){
                this.count2++
            }
        }
    }
</script>