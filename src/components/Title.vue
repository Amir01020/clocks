<template>
    <h2 class="text-[40px] max-w-[448px] font-semibold leading-[44px] tracking-[-0.02em]">{{ title }}</h2>
</template>

<script>

 export default{
    props:{
        title:{
            type:String,
            required:true
        }
    },
 }

</script>