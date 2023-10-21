<template>
  <div>
    <!-- drawer init and show -->
    <section id="sidebar" style="border-right: 0.5px solid #D9D9D9;">
      <div class="hidden lg:flex h-screen flex-col span">
        <div class=" " style="padding: 16px;">
          <div class=" ">
            <div class="">
              <img src="~assets/images/Madesoft-logo.png" class="w-[138px]" alt="">
            </div>
          </div>
        </div>

        <div class="side-menu top  py-5 mt-5" style="padding: 16px;">
          <nav aria-label="Main Nav" class="flex flex-col space-y-4 pt-6">
            <template v-for="(routeItem, index) in routeList" :key="index">
              <router-link
                  :class="[routeItem.names.includes($route.name) ? 'active px-2' : '']"
                  :to="{ path: routeItem.route }"
                  class="flex items-center gap-2 rounded-lg py-2"
              >
               <div>
                 <img  :src="useAsset(routeItem.icon)" alt="" />
               </div>

               <div>
                 <div class=" font-light">{{routeItem.title}}</div>
               </div>
              </router-link>
            </template>

          </nav>

          <nav class="mt-16 flex flex-col px-2">
            <nuxt-link to="" class="flex items-center gap-2 rounded-lg py-2">
              <div>
                <img src="~assets/images/sign-out.svg" alt="" />
              </div>

              <div>
                <div class=" font-light">Log out </div>
              </div>
            </nuxt-link>
          </nav>

        </div>
      </div>


      <div class="relative">
        <transition enter-active-class="transition fade-in-left duration-900"
                    enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100"
                    leave-active-class="transition ease-in duration-295"
                    leave-from-class="transform opacity-100 scale-100"
                    leave-to-class="transform opacity-0 scale-95">
          <div
              v-if="showSidebar"
              :class="[showSidebar ? 'w-48 bg-white z-50' : '']"
              style="background-color: #fff"
              class="lg:hidden flex h-screen absolute flex-col justify-between border-r bg-white">

            <div>
              <div class="inline-flex h-16 w-16 items-center justify-center">
            <span
                class="grid h-10 w-10 place-content-center rounded-lg bg-gray-100 text-xs text-gray-600">
            </span>
              </div>

              <div class="border-t border-gray-100">

                <nav aria-label="Main Nav" class="flex flex-col p-2">
                  <ul class="border-t space-y-6 border-gray-100 pt-4">
                    <li v-for="(routeItem, index) in routeList">
                      <router-link
                          @click="toggleSidebar"
                          :key="index"
                          :class="[
                        routeItem.names.includes($route.name)
                        ? 'text-green-700 '
                        : 'text-white',
                    ]"
                          :to="{ path: routeItem.route }"
                          class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                      >
                        <!--                      <img :src="routeItem.icon" alt="" />-->



                        <div class="flex justify-start mr-auto -align-start">
                          <div class="flex justify-start mr-auto">
                            <img :src="useAsset(routeItem.icon)" class="" />
                          </div>
                          <span  class="relative whitespace-nowrap  top-1/2 ml-7 -translate-y-1/2 rounded bg-black px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100">{{routeItem.title}}</span>
                        </div>
                      </router-link>
                    </li>
                  </ul>
                </nav>
              </div>
            </div>

          </div>

        </transition>

        <div class="pl-6 z-50 absolute top-6 md:hidden">
          <svg
              v-if="!showSidebar"
              @click="toggleSidebar"
              xmlns="http://www.w3.org/2000/svg"
              width="22"
              height="22"
              viewBox="0 0 24 24"
              fill="none"
              stroke="#000000"
              stroke-width="3"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="cursor-pointer"
          >
            <line x1="3" y1="12" x2="21" y2="12"></line>
            <line x1="3" y1="6" x2="21" y2="6"></line>
            <line x1="3" y1="18" x2="21" y2="18"></line>
          </svg>
          <svg
              v-if="showSidebar"
              @click="toggleSidebar"
              xmlns="http://www.w3.org/2000/svg"
              width="22"
              height="22"
              viewBox="0 0 24 24"
              fill="none"
              stroke="#000000"
              stroke-width="4"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="cursor-pointer"
          >
            <line x1="18" y1="6" x2="6" y2="18"></line>
            <line x1="6" y1="6" x2="18" y2="18"></line>
          </svg>
        </div>
      </div>

    </section>
  </div>
</template>

<script setup>
import {useAsset} from "~/composables/useAsset";



const routeList = [
  {
    names: ['index'],
    route: '/',
    title: 'Dashboard',
    icon: '/dashboard.svg',
  },

  {
    names: ['schools'],
    route: '/My-Program/',
    title: 'My-Program',
    icon: '/my-program.svg',
  },
  {
    names: ['students'],
    route: '/community/',
    title: 'Community',
    icon: '/community.svg',
  },
  {
    names: ['staffs','staffs-new','staffs-id'],
    route: '/Schedule/',
    title: 'Schedule',
    icon: '/schedule.svg',
  },
  {
    names: ['customers','customers-id-top-up','customers-id-edit'],
    route: '/Help-Center/',
    title: 'Help Center',
    icon: '/help-center.svg',
  },
  {
    names: ['allocation'],
    route: '/settings/',
    title: 'Settings',
    icon: '/settings.svg',
  },



]
let showSidebar = ref(false);


let toggleSidebar = () => {
  showSidebar.value = !showSidebar.value;
}



</script>

<style scoped>

a{
  color: #C4C4C4!Important;
  /*font-weight: bold;*/
  /*opacity: 0.6;*/
  font-size: 16px!important;

}



.router-link-active {
  border-radius: 4px;
  background: #FFF;
  color: #FF4155!important;
  opacity: inherit!important;
}

.router-link-active span{
  color: #FF4155!important;
  opacity: inherit!important;
}

.router-link-active img {
  filter: brightness(0) invert(1);
}



@media screen and (min-width: 950px) {
  /* SIDEBAR */
  #sidebar {
    position: fixed;
    top: 0;
    left: 0;
    border-right: 0.5px solid #D9D9D9;
    background: #130204;
    box-shadow: 6px 0px 9px 0px rgba(0, 0, 0, 0.10);
    width: 280px;
    padding: 20px;
    height: 100%;
    z-index: 1;
    transition: .3s ease;
    overflow-x: hidden;
    scrollbar-width: none;
  }

  #sidebar::--webkit-scrollbar {
    display: none;
  }

  /* SIDEBAR */


  /* CONTENT */
  #content {
    position: relative;
    width: calc(100% - 260px);
    margin-left: 261px;
    transition: .3s ease;
  }

  #sidebar.hide ~ #content {
    width: calc(100% - 60px);
    left: 60px;
  }
}





/* MAIN */
#content main {
//padding: 36px 10px;
  /*max-height: calc(100vh - 56px);*/
  overflow: hidden !important;
  background: #F9FAFB;
  /*max-width: calc(1050px - 30px);*/
}

/* MAIN */
/* CONTENT */


@media screen and (max-width: 768px) {
  #sidebar {
    width: 200px;
  }

  #content {
    left: 200px;
  }

  #content nav .nav-link {
    display: none;
  }
}


@media screen and (max-width: 576px) {
  #content nav form .form-input input {
    display: none;
  }

  #content nav form .form-input button {
    width: auto;
    height: auto;
    background: transparent;
    border-radius: none;
    color: var(--dark);
  }

  #content nav form.show .form-input input {
    display: block;
    width: 100%;
  }

  #content nav form.show .form-input button {
    width: 36px;
    height: 100%;
    border-radius: 0 36px 36px 0;
    color: var(--light);
    background: var(--red);
  }

  #content nav form.show ~ .notification,
  #content nav form.show ~ .profile {
    display: none;
  }

  #content main .box-info {
    grid-template-columns: 1fr;
  }

  #content main .table-data .head {
    min-width: 420px;
  }

  #content main .table-data .order table {
    min-width: 420px;
  }

  #content main .table-data .todo .todo-list {
    min-width: 420px;
  }
}
</style>