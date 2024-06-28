<template>
    <div class="max-w-[276px] transition cursor-pointer hover:shadow-xl px-5 rounded-xl py-[25px] hover:translate-y-[-20px]">
        <img class="w-full pb-[25px]" :src="img" alt="">
        <p class="text-[14px] text-[#141414]">{{ name }}</p>
        <span class="text-[12px] text-[#14141480]">€{{ price }}</span>
    </div>
</template>

<script>

    export default{
        props:{
            img:{
                type:String,
                required:true,
            },
            name:{
                type:String,
                required:true,
            },
            price:{
                type:String,
                required:true,
            },
        }
    }

</script>