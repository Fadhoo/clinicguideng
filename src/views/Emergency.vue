<template>
    <Navbar/>
    <body>
        <section class="justify-items-center max-w-7xl md:mx-auto px-4">
            <div class="box-content">
                <h3 class="clinicblue text-center pt-4" style="font-weight: 900; font-size: 28px;">Based On Your Location: <br> Lagos, Nigeria.</h3>
                <div class="big-card flex justify-center flex-column justify-self-start mx-auto">
                    <div class="card-body">
                    
                        <hr class="my-8">

                        <div class="grid bg-blue md:grid-rows-3 lg:grid-cols-5 lg:grid-rows-none ">

                            <img class="m-auto" src="../assets/ememergency.png" alt="">
                            
                            <div class="lg:col-span-3 pt-5 pb-5">
                                <h4 class="hospital-name text-center">Lagos State Emergency Service <br> <p class="address-name">767, 112</p></h4>
                            </div>
                            
                            <img class="m-auto" src="../assets/phone.png" alt="" >
                            
                            
                        </div>
                        
                        <hr class="my-8">

                        <div class="grid bg-blue md:grid-rows-3 lg:grid-cols-5 lg:grid-rows-none ">
                            
                            <img class="m-auto" src="../assets/Health.png" alt="">
                            
                            <div class="lg:col-span-3 pt-5 pb-5">
                                <h4 class="hospital-name text-center">Health Emergency Initiative <br> <p class="address-name">08155554459, 08109942450, 08035766767, 08023142807</p></h4>
                            </div>
                                
                            <img class="m-auto" src="../assets/phone.png" alt="">
                            
                            
                        </div>
                        
                        <hr class="my-8">

                        <div class="grid bg-blue md:grid-rows-3 lg:grid-cols-5 lg:grid-rows-none">
                            
                            <img class="m-auto" src="../assets/pills.png" alt="">
                            
                            <div class="lg:col-span-3 pt-5 pb-5">
                                <h4 class="hospital-name text-center">Lagos State Emergency Service<br> <p class="address-name">08023169485, 08059758886</p></h4>
                            </div>
                            
                            <img class="m-auto" src="../assets/phone.png" alt="phone">
                            
                        </div>
                        
                        <hr class="my-8">

                    </div>
                </div>
            </div>
        </section>
        <section class="pt-10">
            <div class="bigger-card" style="height: 718px">
                <div class="container p-20">
                    <h5 class="text-white" style="font-weight:900px; font-size: 70px;">Can’t Find What <br> You’re Looking For?</h5>
                </div>
               
            </div> 
            <div class="bg-clinic-yellow">
                <div class="justify content-center">
                    <p class="text-white text-center">
                    © 2021 Copyright:
                    <a
                    href="#"
                    class="text-white"
                    >Clinic Guide NG. All rights reserved.</a
                    >
                    </p>
                
                </div>
            </div>
        </section>
    </body>
    
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'

export default {
    components: {
        Navbar
    }

}
</script>

<style>
.hospital-name {
    color: white;
    font-size: 35px;
    font-weight: 900;
}

.address-name {
    color:white;
    font-size: 21px;
}
</style>