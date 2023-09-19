<template>
    <div class="bg-gray-100 h-full">
        <div class="container m-auto p-[30px]">
            <div class="flex gap-2 bg-white py-3 px-3 h-[70px] rounded-xl" id="search-bar">
                <div class="bg-gray-200 hover:border border-black duration-300 hover:animate-bounce px-2 items-center w-[200px] gap-2 flex rounded-xl">
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
                    <select class="grow block h-5 bg-gray-200">
                        <option>All</option>
                        <option>Asia</option>
                        <option>Europe</option>
                    </select>
                </div>
                <div class="bg-gray-200 px-2 items-center w-[200px] gap-2 flex rounded-xl">
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
                    <select class="grow block h-5 bg-gray-200">
                        <option>All</option>
                        <option>Asia</option>
                        <option>Europe</option>
                    </select>
                </div>
                <input type="search" class="m-8 bg-red-500">
            </div>
            <div id="conutries" class="flex flex-wrap bg-inherit">
                <p class="w-full m-8">Every Country In America Named asf </p>
                <CountryCard v-for="item in 9" class="basis-1/4 w-1/4 shrink-0"></CountryCard>



            </div>
        </div>


    </div>
</template>