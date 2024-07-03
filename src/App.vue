<template>
    <header class="bg-[#141414]">
        <nav class="flex items-center justify-between py-5 cont">
            <div class="flex items-center gap-20">
                <img src="/logo.svg" alt="">
                <div class="flex gap-5">
                    <a class="text-[#fff] text-[9px]" href="">About us</a>
                    <a class="text-[#fff] text-[9px]" href="">Catalog</a>
                    <a class="text-[#fff] text-[9px]" href="">Sale</a>
                </div>
            </div>
            <button class="bg-[#1E2827] text-white py-3 px-6 rounded-lg shadow-md text-[9px]">
                +380 (68) 443-94-26
            </button>
        </nav>
    </header>

    <main>
        <div class=" bg-[#141414]">
            <div class="flex justify-between cont">
                <h1 class="max-w-[750px] text-white text-[60px] font-[600]">
                    Welcome to our collection of premium watches
                </h1>
                <p class="max-w-[282px] text-white text-[14px]">
                    Our watches are not just timepieces, but also an expression of your personality and lifestyle. From
                    classic designs to modern ones, we have a watch to suit every taste and occasion.
                </p>
            </div>
            <div class="cont flex justify-between items-end gap-[50px] pt-[45px] pb-[80px]">
                <div class="">
                    <div class="w-full bg-[#1E2827] py-[11px] px-[44px] mb-5">
                        <img :src="arr[imgItem].img" alt="">
                    </div>
                    <div class="flex items-center justify-between">
                        <div class="flex gap-3">
                            <div @click="swipe"
                                class="w-10 cursor-pointer hover:opacity-[70%] h-10 border border-solid rotate-180 border-white flex justify-center items-center rounded-[8px]">
                                <img src="/arrov.svg" alt="">
                            </div>
                            <div @click="unSwipe"
                                class="w-10 cursor-pointer hover:opacity-[70%] h-10 border border-solid border-white flex justify-center items-center rounded-[8px]">
                                <img src="/arrov.svg" alt="">
                            </div>
                        </div>
                        <div class="flex gap-[6px] items-center">
                            <p class="text-white text-[14px]">{{ imgItem + 1 }}</p>
                            <div class="w-10 h-[1px] bg-white"></div>
                            <p class="text-white text-[14px]">{{ arr.length }}</p>
                        </div>
                    </div>
                </div>
                <div class="w-[60%]">
                    <img class="w-full" src="/my_times.png" alt="">
                </div>
            </div>
        </div>
        <div class="cont flex justify-between pt-[80px]">
            <div class="">
                <Title title="About us" />
            </div>
            <div class="max-w-[892px]">
                <div class="flex justify-between gap-10 mb-10">
                    <p class="text-[#141414] text-[14px]">
                        Welcome to our premium watch collection, where luxury and style meet functionality and
                        precision. Our
                        selection of timepieces embodies the very best in Swiss craftsmanship and engineering, ensuring
                        that you'll always have a reliable and stylish accessory on your wrist.
                    </p>
                    <p class="text-[#141414] text-[14px]">
                        At our premium watch collection, we believe that a watch is more than just a timekeeping device
                        – it's a statement piece that reflects your personality and style. So why settle for anything
                        less than
                        the best? Browse our collection today and discover the perfect watch for you.
                    </p>
                </div>
                <div class="">
                    <img class="w-full" src="/gif.png" alt="">
                </div>
            </div>
        </div>
        <div class="cont pb-[160px] pt-[160px] flex flex-col">
            <Title title="Catalog" />
            <div class="mt-[60px] flex justify-between gap-5 flex-wrap">
                <List v-for="(item, index) in arr" :key="index" @click="modalClick(clockObj, index, arr)" :img="item.img"
                    :price="item.price" :name="item.name" />

            </div>
       
        </div>
        <div class="cont">
            <Title title="Green And Bronze—The Match Made In Heaven" />
            <div class="flex gap-[25px] justify-between pt-20">
                <div class="w-[48%]">
                    <img src="/image1.png" class="w-full" alt="">
                </div>
                <div class="w-[48%]">
                    <img src="/image2.png" class="w-full" alt="">
                </div>

            </div>
        </div>
        <div class="cont pt-[160px]">
            <Title title="Sale" />
            <div class="max-w-[981px] mt-20 mb-40 mx-auto">
                <div class="flex justify-center gap-10">
                    <div class=" w-[60%] h-[614px]  flex gap-5">
                        <div class="skrol flex flex-col gap-5  w-[25%]">
                            <div v-for="(item, index) in arr" :key="index" @click="swipImg(item.img)"
                                class="flex items-center justify-center w-full bg-black cursor-pointer">
                                <img :src="item.img" class="h-full" alt="">
                            </div>


                        </div>
                        <div class="flex items-center justify-center w-full bg-black">
                            
                            <img :src="imageSwip" class="w-full" alt="">
                        </div>
                    </div>
                    <div class="">
                        <h3 class="text-[38px]">
                            Greenlane Watch By <br>
                            Police For MenHT
                        </h3>
                        <Text text="Product tag: PEWJK2227003" />
                        <p class="text-[18px] mt-[16px]">
                            €700 <span class="text-[12px] text-[#000] opacity-60">€1000</span>
                        </p>
                        <div class="w-full h-[1px] bg-black mt-10"></div>
                        <p class="text-[18px] mb-4">Description</p>
                        <Text
                            text="Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers." />

                        <div class="w-full h-[1px] bg-black mt-5"></div>
                        <p class="text-[18px] mb-4">
                            DETAILS & FEATUREStion
                        </p>
                        <p class="text-[14px]  text-[#000] opacity-60">
                            Gender: man
                            <br>Size: 46x54.5mm
                            <br>Case Colour: Steel
                            <br>Band Material: Metal
                            <br>Case Material: Metal
                            <br>Features: Multifunction
                            <br>Water Resistant: 5 (ATM)
                            <br>Band Colour: Steel
                        </p>
                    </div>
                </div>
                <div class=""></div>
            </div>
        </div>
    </main>
    <footer class="bg-[#1E2827] pt-20 pb-8">
        <div class="cont">
            <div class="flex justify-between mt-[80px]">
                <div class="">
                    <img src="/logo1.svg" class="mb-10" alt="">
                    <div class="mb-5">

                        <a href="" class="text-[18px]  text-white">+380 (68) 443-94-26</a>
                    </div>
                    <a href="" class="text-[18px]  text-white">1678 S. Pioneer Road
                        <br>Salt Lake City
                        <br>UT 84104</a>
                </div>
                <div class="">
                    <div class="mb-5"><a href="" class="text-[18px]  text-white">About Us</a></div>
                    <div class="mb-5"> <a href="" class="text-[18px]  text-white">Catalog</a></div>
                    <div class="mb-5"> <a href="" class="text-[18px]  text-white">Sale</a></div>
                </div>
                <div class="flex self-start gap-4">
                    <a href=""><img class="max-w-[44px] " src="/1.svg" alt=""></a>
                    <a href=""><img class="max-w-[44px] " src="/2.svg" alt=""></a>
                    <a href=""><img class="max-w-[44px] " src="/3.svg" alt=""></a>
                </div>
            </div>
            <div class="flex justify-between mt-40">
                <a href="" class="text-[14px] opacity-55 text-white">©2022 The Watch Spot. All rights reserved.</a>
                <div class="flex gap-5 mt40">
                    <a href="" class="text-[14px] opacity-55 text-white">Privacy Policy</a>
                    <a href="" class="text-[14px] opacity-55 text-white">Terms of Service</a>
                </div>

            </div>
        </div>
    </footer>

    <ModalList :func="modalClick" :price="clockObj.price" :image="clockObj.img" :text="clockObj.text"
        v-if="modal == true" />
</template>

<script>
import List from './components/List.vue'
import Text from './components/Text.vue'
import Title from './components/Title.vue'
import ModalList from './components/ModalList.vue'




export default {
    components: {
        Title,
        List,
        Text,
        ModalList,


    },
    data() {
        return {
            arr: [
                {
                    img: '/clocks/img1.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img2.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img3.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img4.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img5.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img6.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img7.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img8.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img9.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img10.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img11.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                },
                {
                    img: '/clocks/img12.png',
                    name: 'Greenlane Watch By Police For MenHT',
                    price: '700',
                    comment: 'Richly detailed with an understated design - the Police Men’s Greenlane watch features a versatile multifunction design that fits effortlessly into work and play. The steel case is adorned with a semi-transparent black dial. The timepiece exhibits a contrast through a black IP bracelet with matching crown and pushers.'
                }
            ],
            imgItem: 0,
            modal: false,
            clockObj: {
                img: "",
                text: "",
                price: ""
            }, imageSwip:'/clocks/img1.png'
        }
    },
    methods: {
        swipe() {
            if (this.imgItem == 0) {
                this.imgItem = this.arr.length - 1
                return
            }
            this.imgItem -= 1
        },
        unSwipe() {
            if (this.imgItem == this.arr.length - 1) {
                this.imgItem = 0
                return
            }
            this.imgItem += 1
        },
        modalClick(obj, index, arr) {
            this.modal = !this.modal;
            if (this.modal) {
                obj.text = arr[index].name;
                obj.img = arr[index].img;
                obj.price = arr[index].price;
            }
        },
        swipImg(img){
            this.imageSwip = img
        }
    },
}
</script>
