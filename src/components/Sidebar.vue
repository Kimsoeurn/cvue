<template>
    <div class="menu-drawer bg-success">
        <ul>
            <li>
                <img src="./../assets/kimsoeurn.jpeg" alt="Sok Kimsoeurn" class="rounded-circle shadow mb-3" width="120px" height="120px">
            </li>
            <li><a href="index.html" class="text-warning">My Resume</a></li>
            <li><a href="cover_letter.html" class="text-light">Cover Letter</a></li>
            <li><a  href="https://drive.google.com/drive/folders/1HAv9q6n0iBDLNQoN0JA7xkzFIQLvbpKe?usp=sharing" target="_blank" class="text-light">Files & Documents</a></li>
            <li><a href="https://www.linkedin.com/in/kimsoeurn-sok/" target="_blank" class="text-light">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-linkedin mt-0"
                viewBox="0 0 16 16">
                <path
                    d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016a5.54 5.54 0 0 1 .016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z" />
            </svg> LinkedIn</a></li>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'Sidebar'
}
</script>

<style scoped>
.menu-drawer {
    z-index: 1000 !important;
    min-height: 100%;
    width: 0;
    position: fixed;
    right: -550px;
    top: 0;
    transition: right linear 0.2s;
    padding: 50px;
    overflow: hidden !important;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    text-transform: uppercase;
}

.open {
  right: 0px;
  width: 100%;
  transition: right linear 0.2s;
}
.menu-drawer ul {
    list-style-type: none;
    padding-left: 0;
}
.menu-drawer li {
  font-weight: bold;
  margin-bottom: 30px;
  font-size: 1.5rem;
  text-align: center;
}
.menu-drawer li a {
  text-decoration: none;
  color: #ffffff;
}
.menu-drawer li a:hover {
  color: #ffc107 !important;
}
</style>