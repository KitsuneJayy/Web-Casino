<script>
    let num0 = 5;
    function lower() {
        let newnum = getRandomInt(0,9);
        if (newnum < num0) {
            console.log("Win by "+newnum);
        } else {
            console.log("Lose by "+newnum);
        }
        num0 = newnum;
    }
    function higher() {
        let newnum = getRandomInt(0,9);
        if (newnum > num0) {
            console.log("Win by "+newnum);
        } else {
            console.log("Lose by "+newnum);
        }
        num0 = newnum;
    }
    function getRandomInt(min, max) {
        min = Math.ceil(min);
        max = Math.floor(max);
        return Math.floor(Math.random() * (max - min + 1)) + min;
    }

</script>
<div class="game-container flex flex-col justify-center item-center min-h-screen">


<ul role="list" class="max-w-sm divide-y divide-gray-200 dark:divide-gray-700">
    <li class="py-3 sm:py-4">
        <div class="flex items-center space-x-3 rtl:space-x-reverse">
            <div class="shrink-0">
                <img class="w-10 h-10 rounded-full" src="/docs/images/people/profile-picture-5.jpg" alt="Neil image">
            </div>
            <div class="flex-1 min-w-0">
                <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">
                    Earth Casino
                </p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">
                    Money : $1000
                </p>
            </div>
            <span class="inline-flex items-center bg-green-100 text-green-800 text-xs font-medium px-2.5 py-0.5 rounded-full dark:bg-green-900 dark:text-green-300">
                <span class="w-2 h-2 me-1 bg-green-500 rounded-full"></span>
                Available
            </span>
        </div>
    </li>
    <!-- <li class="py-3 sm:py-4">
        <div class="flex items-center space-x-3 rtl:space-x-reverse">
            <div class="shrink-0">
                <img class="w-8 h-8 rounded-full" src="/docs/images/people/profile-picture-4.jpg" alt="Neil image">
            </div>
            <div class="flex-1 min-w-0">
                <p class="text-sm font-semibold text-gray-900 truncate dark:text-white">
                    Bonnie Green
                </p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">
                    email@flowbite.com
                </p>
            </div>
            <span class="inline-flex items-center bg-red-100 text-red-800 text-xs font-medium px-2.5 py-0.5 rounded-full dark:bg-red-900 dark:text-red-300">
                <span class="w-2 h-2 me-1 bg-red-500 rounded-full"></span>
                Unavailable
            </span>
        </div>
    </li> -->
</ul>
    <div class="card-container relative items-center justify-center">
        <img src="https://unocardinfo.victorhomedia.com/graphics/uno_card-red1.png" class="card relative">
    </div>
    <div class="divButton flex justify-items-center gap-10 mt-10">
        
            <button on:click={lower} class="lowerButton ml-11 relative inline-flex items-center justify-center p-0.5 mb-2 me-2 overflow-hidden text-m font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-purple-600 to-blue-500 group-hover:from-purple-600 group-hover:to-blue-500 hover:text-white dark:text-white focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800">
            <span class="relative px-10 py-4 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">
            Lower
            </span>
            </button> 

            <button on:click={higher} class="higherButton relative inline-flex items-center justify-center p-0.5 mb-2 me-2 overflow-hidden text-sm font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-red-200 via-red-300 to-yellow-200 group-hover:from-red-200 group-hover:via-red-300 group-hover:to-yellow-200 dark:text-white dark:hover:text-gray-900 focus:ring-4 focus:outline-none focus:ring-red-100 dark:focus:ring-red-400">
            <span class="relative px-10 py-4 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">
            Higher
            </span>
            </button>
    </div>
</div>