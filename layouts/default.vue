<template>
  <div>
    <!-- drawer init and show -->
    <section id="sidebar">
      <SideBar />

    </section>

    <section id="content">

      <div style="box-shadow: 0px 3px 7px 0px rgba(0, 0, 0, 0.06); height: 75px;">
        <TopNav class="shadow-md" />
      </div>



      <main class="">
        <div class="w-full h-screen sticky top-0 overflow-y-auto">
          <slot class=""/>
        </div>
      </main>


    </section>

  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>



.active img {
  filter: brightness(0) invert(1)!important;
}

.active span{
  opacity: inherit!important;
}

@media screen and (min-width: 950px) {


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
    width: calc(100% - 50px);
    left: 40px;
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