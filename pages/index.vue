<template>
  <div class="h-screen w-full bg-black">
     <div class="flex h-full">
        <div class="bg-gray-300 w-1/3 ">
           <div class="flex justify-center h-full items-center">
             <div class="justify-center" @click="timerCountDown()">
              <svg  height="200px" width="200px" version="1.1" id="_x32_" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512 512" xml:space="preserve" fill="#000000">
                 <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                 <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                 <g id="SVGRepo_iconCarrier">
                    <g>
                       <path class="st0" d="M115.343,123.839c0.814,1.256,3.343,2.605,7.23,4.014c7.586-1.069,14.943-1.586,21.885-1.586 c15.579,0,30.166,2.469,42.438,7.145c17.87-5.567,43.412-11.694,69.108-11.694c25.694,0,51.228,6.126,69.108,11.694 c12.262-4.676,26.848-7.145,42.42-7.145c7.001,0,14.418,0.518,22.063,1.604c3.471-1.341,6.296-2.699,8.325-4.031 c42.2-28.139,53.036-81.183,47.41-69.931c-4.218,8.418-60.309,35.581-100.004,52.222c14.68-17.769,31.677-44.134,43.438-80.309 c0,0-60.978,52.382-98.867,74.887c-11.974-20.816-33.892-86.589-33.892-86.589s-18.567,49.515-20.358,81.412 c-30.21-16.929-63.354-51.474-72.485-74.538c-10.752-27.189-13.78,53.545,15.436,89.396c-1.095,0.162-2.206,0.315-3.344,0.476 c-39.111-16.072-100.454-47.91-104.926-54.86C64.708,47.255,73.143,101.954,115.343,123.839z M290.531,107.181l0.747,0.857 l-3.098-0.746L290.531,107.181z"></path>
                       <path class="st0" d="M485.83,198.564c-38.169-57.253-117.544-70.584-160.338-52.195c-18.27-5.906-43.872-12.27-69.49-12.27 c-25.619,0-51.228,6.364-69.499,12.27c-42.794-18.388-122.168-5.058-160.338,52.195c-64.136,96.203-18.711,299.318,229.836,299.318 C504.541,497.882,549.974,294.767,485.83,198.564z M101.172,262.929c-17.099,0-30.947-13.857-30.947-30.948 c0-17.09,13.848-30.947,30.947-30.947c17.082,0,30.947,13.857,30.947,30.947C132.119,249.071,118.253,262.929,101.172,262.929z"></path>
                    </g>
                 </g>
              </svg>
              <div class="mx-auto " ><span class="text-8xl font-bold w-full">{{ minute }}:<span v-if="second <10">0</span>{{ second }}</span></div>
           </div>

              
           </div>
        </div>
        <div class="bg-white w-2/3">
          <div class="flex justify-end justify-items-end w-full  p-8">
            <div class="px-4 h-1/18 justify-center flex">
              <svg class="w-10 mx-7" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g id="analysis"> <polyline class="cls-1" points="3.96 14.04 9 9 15 15 23 7"></polyline> <line class="cls-1" x1="2.54" y1="15.46" x2="1" y2="17"></line> </g> </g></svg>
              <span class="mx-7 text-lg">Statics</span>
              <svg class="w-10 mx-7" viewBox="0 0 20 20" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <title>profile_image_round [#1326]</title> <desc>Created with Sketch.</desc> <defs> </defs> <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"> <g id="Dribbble-Light-Preview" transform="translate(-380.000000, -2199.000000)" fill="#000000"> <g id="icons" transform="translate(56.000000, 160.000000)"> <path d="M342,2055.615 C342,2055.722 341.97,2055.821 341.939,2055.918 C341.723,2052.974 339.918,2050.482 337.375,2049.283 C338.368,2048.369 339,2047.071 339,2045.615 C339,2043.534 337.728,2041.753 335.92,2041 L341,2041 C341.552,2041 342,2041.063 342,2041.615 L342,2055.615 Z M339.963,2057 L327.975,2057 C327.974,2057 327.969,2056.741 327.969,2056.701 C327.969,2053.605 330.326,2050.96 333.339,2050.645 C334,2050.733 334.255,2050.622 334.623,2050.576 C337.625,2050.902 339.969,2053.623 339.969,2056.71 C339.969,2056.75 339.964,2057 339.963,2057 L339.963,2057 Z M326,2055.615 L326,2041.615 C326,2041.063 326.448,2041 327,2041 L332.08,2041 C330.272,2041.753 329,2043.534 329,2045.615 C329,2047.06 329.622,2048.351 330.602,2049.264 C328.107,2050.422 326.307,2052.82 326.012,2055.675 C326.011,2055.654 326,2055.636 326,2055.615 L326,2055.615 Z M337,2045.615 C337,2047.055 335.979,2048.26 334.623,2048.548 C334.033,2048.5 333.868,2048.508 333.368,2048.545 C332.017,2048.254 331,2047.052 331,2045.615 C331,2043.961 332.346,2042.615 334,2042.615 C335.654,2042.615 337,2043.961 337,2045.615 L337,2045.615 Z M342,2039 L326,2039 C324.895,2039 324,2039.895 324,2041 L324,2057 C324,2058.104 324.895,2059 326,2059 L342,2059 C343.105,2059 344,2058.104 344,2057 L344,2041 C344,2039.895 343.105,2039 342,2039 L342,2039 Z" id="profile_image_round-[#1326]"> </path> </g> </g> </g> </g></svg>
              <span class="mx-7 text-lg">Profile</span>
            </div>
          </div>
          <div class="w-full py-200 h-1/3 my-12" v-if="timerIsStarted">
            
            <div class="w-1/2 py-1 mx-auto">
              <h1 class="text-lg font-bold">NEW TASK</h1>
              <input class="block w-full mt-10 h-12 border-2 border-black px-3 font-bold text-black" v-model="name" type="text" placeholder="Name" />
              <span v-if="nameIsValid === false" class="text-red-500">THIS FIELD IS REQUIRED!</span>
              <input class="block w-full mt-10 h-12 border-2 border-black px-3 font-bold" v-model="email" type="text" placeholder="Email"/>
              <span v-if="mailIsValid === false" class="text-red-500">EMAIL FORMAT IS INVALID!</span>
              <button class="block w-full mt-8 h-12 border-2 border-black bg-black rounded-2xl" @click="submit()"><span class="text-white">START</span></button>
              <button class="block w-full mt-4 h-12 border-2 bg-gray-300 rounded-2xl" ><span class="text-color">CANCEL</span></button>
            </div>
          </div>
        </div>
     </div>
  </div>
</template>
<script setup>

  const name = ref('')
  const timerIsStarted = ref(false)
  const emailRegex = /^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$/;
  const email = ref('')
  const second = ref(0)
  const minute = ref(25)
  const mailIsValid =ref()
  const nameIsValid = ref()
  const timerCountDown = () =>{
    if(!timerIsStarted.value){
    setInterval(() =>{
      timerIsStarted.value =true;
        if(second.value != 0){
          second.value--
        }
        else{
          minute.value--
          second.value = 59
        }
    },1000)

  }
  }
  const submit = () =>{
    validateData();
  }
  const validateData = () =>{
    mailIsValid.value = validateEmail(email.value)
    nameIsValid.value = validateName(name.value)
  }
  const validateEmail = (email) =>{
    return emailRegex.test(email);
  }
  const validateName = (name) =>{
    return name.trim() !== "";
  }
</script>
<style scoped></style>