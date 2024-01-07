<template>
    <div>
        <vs-navbar collapse v-model="activeItem" :color="colorx" text-color="rgba(255,255,255,.6)"
            active-text-color="rgba(255,255,255,1)" class="nabarx">
            <div>
                <vs-navbar-title>
                    QR Code Genarator
                </vs-navbar-title>
            </div>

            <vs-navbar-item index="0">
                <a href="#">Home</a>
            </vs-navbar-item>
            <vs-navbar-item index="1">
                <a href="#">News</a>
            </vs-navbar-item>
            <vs-navbar-item index="2">
                <a href="#">Update</a>
            </vs-navbar-item>
        </vs-navbar>
    </div>
</template>
<script>
export default {
    name: 'NavBar',
    data() {
        return {
            colorx: '#8C5E58',
        }
    },
}
</script>
  