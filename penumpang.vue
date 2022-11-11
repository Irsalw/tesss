<template>
    <div id="app" class="container mt-4">
        <div class="card">
            <div class="card-body">
                <div v-for="item, index in form" :key="item">
                    <h3>Data Penumpang {{index+1}}</h3>
                    <div class="row" >
                        <div class="col-sm-5">
                            <label>Nama</label>
                            <input type="text" class="form-control" v-model="item.nama">
                        </div>
                        <div class="col-sm-5">
                            <label>Umur</label>
                            <input type="number" class="form-control" v-model="item.umur">
                        </div>
                        <div class="col-sm-5">
                            <label>Alamat</label>
                            <input type="text" class="form-control" v-model="item.alamat">
                        </div>
                        <div class="col-sm-2 pt-4">
                            <button type="button" class="btn btn-danger btn-sm" @click="removeRow(index)" >x</button>
                            <button type="button" class="btn btn-success btn-sm" @click="addRow">+</button>
                        </div>
                    </div> 
                </div>
                <button type="button" class="btn btn-success mt-3" @click="saveItem">SAMPAN</button>
            </div>
        </div>
    </div>
</template>

<script>
import {reactive} from 'vue'
export default{
    name: 'hello world',
	setup(){
		const form = reactive([
		{Nama : '', Umur : 0, Alamat : ''}
		])
        
        const addRow = () => {
            form.push({nama : '', umur : 0, alamat : ''})
        }
        const removeRow = (index) +> {
            if(form.length > 1){
                form.splice(index,1)
            }
            
        }
        const saveItem = () => {
            
            })
        }
        return (
            form,
            addRow,
            removeRow,
            saveItem
        )
	}
}
</script>