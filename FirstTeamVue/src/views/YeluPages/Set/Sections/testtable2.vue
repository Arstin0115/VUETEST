<style>
.book {
    border: 1px solid #ccc;
    border-radius: 10px;
    width: 200px;
    height: 350px;
    margin: 10px;
    padding: 10px;
    background-color: black;
    color: white;


}
</style>

<template>
    <div class="row">
        <div class="col-lg-9 z-index-2 border-radius-xl mx-auto py-3">
            <div class="row">
                <div class="col-md-4 position-relative book" v-for="item in MemberInfo">


                    <p hidden>{{ item.活動id }}</p>

                    <p>{{ item.地區 }}</p>



                </div>

            </div>
        </div>
    </div>
</template>

<script setup>

import { ref, reactive, onMounted, computed } from 'vue'
import axios from "axios";

const webApiBaseAddr = ref("https://localhost:7219/api/ActDetails");

let MemberInfo = reactive([])


// const filter = ref("")
// const employeeId = ref(null)
// const firstName = ref(null)
// const lastName = ref(null)
// const title = ref(null)
// const firstNameOld = ref(null)
// const lastNameOld = ref(null)
// const titleOld = ref(null)
// let employeeList = reactive([])

const getEmployeeDTOes = onMounted(() => {
    axios
        .get(webApiBaseAddr.value)
        .then(res => {
            console.log(res.data)
            //employeeDTOes=res.data;
            MemberInfo.splice(0, res.data.length, ...res.data)

        })
        .catch((err) => {
            console.error(err);
        })

})

</script>


