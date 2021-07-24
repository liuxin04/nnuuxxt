<template>
    <div>
        <div ref="qrCodeUrl" class="qrcode"></div>
    </div>
</template>
<script>
export default {
    mounted() {
        this.creatQrCode();
    },
    methods: {
        creatQrCode() {
            var qrcode = new this.Qcode(this.$refs.qrCodeUrl, {
                text: "xxxx", // 需要转换为二维码的内容
                width: 100,
                height: 100,
                colorDark: "#000000",
                colorLight: "#ffffff",
                correctLevel: this.Qcode.CorrectLevel.H
            });
        }
    }
};
</script>
<style></style>
