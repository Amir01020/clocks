<template>
    <p class="text-[14px] max-w-[369px] text-[#000] opacity-60">
        {{ text }}
    </p>
</template>

<script>

export default{
    props:{
        text:{
            type:String,
            required:true
        }
    }
}

</script>