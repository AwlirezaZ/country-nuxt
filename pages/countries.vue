<template>
    <div class="w-[1264px] m-auto">
      <div class="bg-white w-full p-2 h-[77px] rounded-xl flex gap-4 mt-[200px] flex items-center">
        <div class="bg-gray-200 w-[319px] h-[53px] p-4 flex items-center rounded-xl">
          <div class="h-[37px] w-full relative rounded-xl flex items-center gap-4">
            <span class="opacity-20 text-sm absolute -top-1 left-[16%]">continent</span>
            <div class="border-r border-black border-opacity-20 pr-2">
              <svg width="18" height="19" fill="#000000" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path d="M12,1A11,11,0,1,0,23,12,11.013,11.013,0,0,0,12,1ZM8.149,3.878A4.063,4.063,0,0,1,7.376,6.07c-.394-.2-.86-.457-1.378-.757A9.025,9.025,0,0,1,8.149,3.878ZM6.183,18.855a9,9,0,0,1-2.992-5.012c3.609-1.225,5.149-1.41,5.749-1.41h0a1.775,1.775,0,0,1-.523.735,2.157,2.157,0,0,0-.648.959,1.485,1.485,0,0,0,.5,1.523c.046.427-.983,1.762-1.664,2.646C6.465,18.476,6.324,18.67,6.183,18.855ZM12,21a8.937,8.937,0,0,1-4.156-1.025c.115-.152.231-.311.344-.458,1.353-1.755,2.748-3.566,1.709-5A3.382,3.382,0,0,0,11,12a1.452,1.452,0,0,0-.619-1.2c-.463-.327-1.395-.989-7.371.992A8.941,8.941,0,0,1,4.64,6.837c.738.436,1.379.791,1.913,1.058a1.838,1.838,0,0,0,1.92-.152c1.12-.784,1.7-2.8,1.713-4.559a8.911,8.911,0,0,1,4.787.331C11.758,4.888,11,6.653,11,8c0,3.034,2.017,3.268,3.1,3.394.9.105.9.105.9.606a6.574,6.574,0,0,1-.526,2.455c-.363.973-.911,2.445,1.079,3.44a2.339,2.339,0,0,0,1.061.243,6.4,6.4,0,0,0,2.643-.837A8.987,8.987,0,0,1,12,21Zm8.635-6.485a14.445,14.445,0,0,0-1.969.851c-.786.387-1.862.917-2.219.739a2.835,2.835,0,0,1-.336-.193,4.1,4.1,0,0,1,.237-.76A8.476,8.476,0,0,0,17,12c0-2.283-1.8-2.492-2.67-2.593C13.282,9.286,13,9.253,13,8c0-1.628,2.545-2.677,4.354-3.217a8.939,8.939,0,0,1,3.281,9.732Z"></path></g></svg>
  
  
            </div>
            <select v-model="selectedContinent" class="w-full pt-4 bg-gray-200 focus:outline-none" name="cars" id="cars">
              <option value="all">All</option>
              <option v-for="continent in continents" :value="continent">
                {{ continent }}
              </option>
            </select>
          </div>
        </div>
        <div class="bg-gray-200 w-[319px] h-[53px] p-4 flex items-center rounded-xl">
          <div class="h-[37px] w-full relative rounded-xl flex items-center gap-4">
            <span class="opacity-20 text-sm absolute -top-1 left-[16%]">name</span>
            <div class="border-r border-black border-opacity-20 pr-2">
              <svg width="18" height="19" viewBox="0 0 18 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_53_46)">
                  <path
                    d="M17.671 16.5841L14.1871 13.0988C16.7939 9.61519 16.0831 4.67794 12.5996 2.07115C9.11598 -0.535637 4.17873 0.17515 1.57194 3.65873C-1.03485 7.14231 -0.324064 12.0796 3.15952 14.6863C5.95782 16.7803 9.80122 16.7803 12.5996 14.6863L16.0849 18.1717C16.5229 18.6097 17.233 18.6097 17.671 18.1717C18.109 17.7337 18.109 17.0236 17.671 16.5856L17.671 16.5841ZM7.90858 14.0136C4.81254 14.0136 2.30273 11.5038 2.30273 8.4078C2.30273 5.31176 4.81254 2.80195 7.90858 2.80195C11.0046 2.80195 13.5144 5.31176 13.5144 8.4078C13.5111 11.5024 11.0033 14.0104 7.90858 14.0136Z"
                    fill="#374957" />
                </g>
                <defs>
                  <clipPath id="clip0_53_46">
                    <rect width="18" height="18" fill="white" transform="translate(0 0.5)" />
                  </clipPath>
                </defs>
              </svg>
              
            </div>
            <input v-model="userCountryNameSearch" class="grow rounded-xl pt-4 h-10 bg-gray-200 focus:outline-none" type="text" />
          </div>
        </div>
      </div>
      <div class="bg-white w-full p-2 rounded-xl mt-10">
        <h1 class="text-lg font-bold pl-2 mb-6">Every country in {{selectedContinent}} named</h1>
        <ul class="flex flex-wrap">
          <CountryCard v-for="country in filteredCountries" class="basis-1/4 px-2 mb-6">
            <NuxtLink class="w-[296px]" to="/">
              <div class="pl-2 bg-gray-200 w-[296px] h-[162px] rounded-r-xl">
                <img class="w-full h-full rounded-r-xl" :src="country.flags.png" :alt="country.flags.alt">
              </div>
              <div class="flex gap-3 items-center mt-2">
                <span class="font-semibold">{{ country.name.common }}</span>
                <span class="text-xs text-opacity-80 text-gray-400">{{country.region}}</span>
              </div>
            </NuxtLink>
          </CountryCard>
        </ul>
      </div>
    </div>
    
  </template>
  
  <script setup>
  import {uniq} from 'lodash'
    const countries = ref()
    const selectedContinent = ref('all')
    const filteredCountries = ref()
    const userCountryNameSearch = ref('')
    const continents = ref()
  const getCountries = async (query) => {
      const url = query ? `https://restcountries.com/v3.1/name/${query}` : 'https://restcountries.com/v3.1/all'
      const response = await fetch(url);
      countries.value = await response.json();
      console.log(countries.value)
      filteredCountries.value= countries.value
      continents.value = uniq(countries.value.map((country) => country.region))
  }
  onMounted(() => {
      getCountries();
  })  
  
  watch(userCountryNameSearch,()=>{
    if(!userCountryNameSearch.value){
      filteredCountries.value = countries.value
    }
    else{
      filteredCountries.value = countries.value.filter((country) => country.name.common.toLowerCase().includes(userCountryNameSearch.value.toLowerCase()))
    }
  })
  watch(selectedContinent,()=>{
    if(selectedContinent.value === 'all'){
      filteredCountries.value = countries.value
    }
    else if(selectedContinent.value){
      filteredCountries.value = countries.value.filter((country) => country.region.toLowerCase().includes(selectedContinent.value.toLowerCase()))
    }
  })
  </script>
  
  <style lang="scss" scoped></style>
  