<script setup>
const router = useRouter()
onMounted(() => {
    const button1 = document.querySelector(".button1");
    const button2 = document.querySelector(".button2");
    const button3 = document.querySelector(".button3");
    const button4 = document.querySelector(".button4");
    button1.onclick = function () {
        button1.style.backgroundColor = 'rgba(255, 255, 255, 0.2)';
        button2.style.backgroundColor = '#454545';
        button3.style.backgroundColor = '#454545';
        button4.style.backgroundColor = '#454545';
    };
    button2.onclick = function () {
        button2.style.backgroundColor = 'rgba(255, 255, 255, 0.2)';
        button1.style.backgroundColor = '#454545';
        button3.style.backgroundColor = '#454545';
        button4.style.backgroundColor = '#454545';
    };
    button3.onclick = function () {
        button3.style.backgroundColor = 'rgba(255, 255, 255, 0.2)';
        button1.style.backgroundColor = '#454545';
        button2.style.backgroundColor = '#454545';
        button4.style.backgroundColor = '#454545';
    };
    button4.onclick = function () {
        button4.style.backgroundColor = 'rgba(255, 255, 255, 0.2)';
        button1.style.backgroundColor = '#454545';
        button2.style.backgroundColor = '#454545';
        button3.style.backgroundColor = '#454545';
    };
})
</script>

<template>
    <aside class="h-screen bg-[#454545] px-4 py-6 flex flex-col">
        <h2 class="text-[25px] mb-4 text-white flex items-center w-[350px]">
            <button @click="router.go(-1)">
                <img class="w-[28px] h-[15px]" src="../public/backicon.png" alt="">
            </button>
            Admin Panel
        </h2>
        <div class="mt-[12px]">
            <nuxt-link to="/admin/dashboard">
                <button
                    class="button1 sidebar_item flex text-[#fff] w-[250px] hover:bg-[#fff]/20 items-center rounded-[8px]  h-[40px] p-[5px]">
                    <img class="w-[21px] h-[19px] mr-[20px]" src="../public/adminpane.png" alt=""> Dashboard
                </button></nuxt-link>
            <nuxt-link to="/admin/create-product">
                <button
                    class="button2 sidebar_item flex text-[#fff] w-[250px] mt-[5px] hover:bg-[#fff]/20 items-center rounded-[8px]  h-[40px] p-[5px]">
                    <img class="w-[21px] h-[19px] mr-[20px]" src="../public/createproducticon.png" alt=""> Create product
                </button></nuxt-link>
            <nuxt-link to="/admin/manage-product">
                <button
                    class=" button3 sidebar_item mt-[5px] flex text-[#fff] w-[250px] hover:bg-[#fff]/20 items-center rounded-[8px]  h-[40px] p-[5px]">
                    <img class="w-[21px] h-[19px] mr-[20px]" src="../public/adminpane.png" alt=""> Manage product
                </button></nuxt-link>
            <nuxt-link to="/admin/orders">
                <button
                    class="button4 sidebar_item mt-[5px] flex text-[#fff] w-[250px] hover:bg-[#fff]/20 items-center rounded-[8px]  h-[40px] p-[5px]">
                    <img class="w-[21px] h-[19px] mr-[20px]" src="../public/adminpane.png" alt=""> Orders
                </button></nuxt-link>
        </div>
    </aside>
</template>

<style scoped>
.router-link-active {
    background-color: #fff;
    color: black;
}
</style>