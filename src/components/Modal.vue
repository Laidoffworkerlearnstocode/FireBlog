<template lang="">
    <div class="modal flex justify-center items-center z-50 absolute w-full h-full top-0 bg-modal_bg">
        <div class="modal-content flex flex-col space-y-4 rounded-md w-72 py-10 px-8 bg-white">
            <p class="text-center"> {{ modalData_Store.message }} </p>
            <button class="self-center bg-gray-700 text-white rounded-full w-28 py-2 px-4 hover:bg-gray-500" @click="closeModal">知道了</button>
        </div>
        
    </div>
</template>
<script>
import {modalDataStore} from "../store/index.js";

export default {
    name: 'Modal',
    data() {
        const modalData_Store = modalDataStore();
        return {
            modalData_Store
        }
    },
    methods: {
        closeModal() {
            this.modalData_Store.modalShow = false;
        }
    },
}
</script>
<style lang="">
    
</style>