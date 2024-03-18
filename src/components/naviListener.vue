<template>
    <div>
        User Agent: {{ userAgent }}
        <br>
        Network Changed: {{ networkChanged }}
    </div>
</template>

<script>
export default {
    name: "NaviListener",
    data() {
        return {
            userAgent: navigator.userAgent,
            networkChanged: 0,
        };
    },
    mounted() {
        if (navigator.connection) {
            navigator.connection.addEventListener('change', this.handleConnection);
        } else {
            console.log("Network Information API is not supported in this browser.");
        }
    },
    beforeDestroy() {
        if (navigator.connection) {
            navigator.connection.removeEventListener('change', this.handleConnection);
        }
    },
    methods: {
        handleConnection() {
            this.networkChanged += 1;
            // alert("Network Changed");
        },
    },
}

</script>
