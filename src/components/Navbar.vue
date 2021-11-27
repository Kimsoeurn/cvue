<template>
        <header class="d-print-none">
        <nav class="navbar navbar-expand-lg navbar-dark bg-success">
            <div class="container-fluid">
                <router-link to="/" class="navbar-brand">My Resume</router-link>
                <a class="toggle-menu d-sm-none d-block" href="#">
                    <i></i>
                    <i></i>
                    <i></i>
                </a>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        <li class="nav-item">
                            <router-link to="/cover-letter" class="nav-link">Cover Letter</router-link>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="https://drive.google.com/drive/folders/1HAv9q6n0iBDLNQoN0JA7xkzFIQLvbpKe?usp=sharing" target="_blank">Files & Documents</a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
        <div class="container mt-3">
            <a href="#" onclick="downloadPdf()"
             class="btn btn-primary me-1"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cloud-download"
                viewBox="0 0 16 16">
                <path
                    d="M4.406 1.342A5.53 5.53 0 0 1 8 0c2.69 0 4.923 2 5.166 4.579C14.758 4.804 16 6.137 16 7.773 16 9.569 14.502 11 12.687 11H10a.5.5 0 0 1 0-1h2.688C13.979 10 15 8.988 15 7.773c0-1.216-1.02-2.228-2.313-2.228h-.5v-.5C12.188 2.825 10.328 1 8 1a4.53 4.53 0 0 0-2.941 1.1c-.757.652-1.153 1.438-1.153 2.055v.448l-.445.049C2.064 4.805 1 5.952 1 7.318 1 8.785 2.23 10 3.781 10H6a.5.5 0 0 1 0 1H3.781C1.708 11 0 9.366 0 7.318c0-1.763 1.266-3.223 2.942-3.593.143-.863.698-1.723 1.464-2.383z" />
                <path
                    d="M7.646 15.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 14.293V5.5a.5.5 0 0 0-1 0v8.793l-2.146-2.147a.5.5 0 0 0-.708.708l3 3z" />
            </svg> Download</a>
            <a href="#" onclick="window.print()" class="btn btn-secondary"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-printer"
                viewBox="0 0 16 16">
                <path d="M2.5 8a.5.5 0 1 0 0-1 .5.5 0 0 0 0 1z" />
                <path
                    d="M5 1a2 2 0 0 0-2 2v2H2a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h1v1a2 2 0 0 0 2 2h6a2 2 0 0 0 2-2v-1h1a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2h-1V3a2 2 0 0 0-2-2H5zM4 3a1 1 0 0 1 1-1h6a1 1 0 0 1 1 1v2H4V3zm1 5a2 2 0 0 0-2 2v1H2a1 1 0 0 1-1-1V7a1 1 0 0 1 1-1h12a1 1 0 0 1 1 1v3a1 1 0 0 1-1 1h-1v-1a2 2 0 0 0-2-2H5zm7 2v3a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1v-3a1 1 0 0 1 1-1h6a1 1 0 0 1 1 1z" />
            </svg> Print</a>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Sidebar',
  mounted() {
    window.$(".toggle-menu").click(function () {
        window.$(this).toggleClass("active");
        window.$('.menu-drawer').toggleClass("open");
        window.$('.cv').toggleClass('d-none');
    });
  }
}
</script>

<style scoped>
.toggle-menu {
  width: 50px;
  height: 50px;
  display: inline-block;
  position: relative;
  top: 0;
  float: right;
  z-index: 1000;
}

.toggle-menu i {
  position: absolute;
  display: block;
  height: 2px;
  background: #ffc107;
  width: 30px;
  left: 0px;
  -webkit-transition: all 0.3s;
  transition: all 0.3s;
}

.toggle-menu i:nth-child(1) {
  top: 16px;
}

.toggle-menu i:nth-child(2) {
  top: 24px;
}

.toggle-menu i:nth-child(3) {
  top: 32px;
}

.toggle-menu.active i:nth-child(1) {
  top: 25px;
  -webkit-transform: rotateZ(45deg);
  transform: rotateZ(45deg);
}

.toggle-menu.active i:nth-child(2) {
  background: transparent;
}

.toggle-menu.active i:nth-child(3) {
  top: 25px;
  -webkit-transform: rotateZ(-45deg);
  transform: rotateZ(-45deg);
}
</style>