<template>
    <div class="fixed w-full flex justify-center  items-center h-full top-0 left-0 z-20 bg-[#0000006f]">
        <div class="bg-white max-w-[940px] justify-center  relative gap-5 flex p-10">
            <img src="/x.svg" @click="func" class="absolute right-5 cursor-pointer top-5" alt="">
            <div class="">
                <img :src="image" class="w-full" alt="">
                <p class="text-[14px]">{{ text }}</p>
                <span class="text-[12px] text-[#14141480]">€{{ price }}</span>
            </div>
            <div class="w-[60%]">
                <p class="text-[14px] mb-[12px] ">Full name</p>
                <input placeholder="Enter your full name"
                    class="p-2 w-full outline-none h-10 border border-[#14141480] border-solid rounded-md " type="text">
                <p class="text-[14px] mb-[12px] mt-[24px]">Email</p>
                <input placeholder="Enter your email"
                    class="p-2 w-full outline-none h-10 border border-[#14141480] border-solid rounded-md " type="text">
                <p class="text-[14px] mb-[12px] mt-[24px]">Card number</p>
                <input placeholder="Enter card"
                    class="p-2 w-full h-10 outline-none border border-[#14141480] border-solid rounded-md " type="text">
                <p class="text-[14px] mb-[12px] mt-[24px]">Comments</p>
                <textarea name="" id=""
                    class="p-2 w-full border outline-none max-h-[166px] min-h-[166px] border-[#14141480] border-solid rounded-md "
                    placeholder="Enter your text" cols="30" rows="10"></textarea>
                <button class="w-full h-12 rounded-md mt-10 bg-[#1E2827] text-[12px] text-white">submit</button>
                <p class="text-[12px] opacity-60 mt-[12px]">
                    By clicking on “Submit” button, you agree to our Privacy Policy,
                    and allow Promodo to use this information for marketing purposes.
                </p>
            </div>
        </div>
    </div>
</template>


<script>

export default{
    props:{
        func:{
            type:Function,
            required:true
        },
        image:{
            type:String,
            required:true
        },
        text:{
            type:String,
            required:true
        },
        price:{
            type:String,
            required:true
        },
    }
}

</script>