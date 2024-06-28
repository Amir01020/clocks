<template>
    <div class="max-w-[276px] py-[25px]">
        <img class="w-full pb-[25px]" :src="img" alt="">
        <p class="text-[14px] text-[#141414]">{{ name }}</p>
        <span class="text-[12px] text-[#14141480]">{{ price }}</span>
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