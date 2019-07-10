<template>
    <main>
        <p>select a file</p>
        <input style="display:none;" ref="fileinput" type="file" @change="uploadFile">
        <button @click="$refs.fileinput.click()">pickFile</button>
        <button class="success white--text ma-3 px-2 py-1" @click="submitFile">Send</button>
    </main>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return{
            uploadedfile: null,
        }
    },
    methods:{
        uploadFile(event){
            console.log(event)
            this.uploadedfile = event.target.files[0];
        },
        submitFile(){
            const fd = new FormData();
            fd.append("image" , this.uploadedfile , this.uploadedfile.name);
            axios.post("https://url" , fd ,{
                onUploadProgress: uploadEvent =>{ // its very usefull for progress bar :)
                    console.log("the progress is: " + math.round(uploadEvent.loaded / uploadEvent.total *100) + "%" )
                }
            })
        }
    }
}
</script>

<style>

</style>
