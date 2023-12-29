<template>
<div>
    <section>
        <h3>Añadir profesor</h3>
        <div><label>Nombre: </label><input type="text" v-model="teacher.teachername"/></div>
        <div><label>Apellido: </label><input type="text" v-model="teacher.surname"/></div>
        <div><label>DNI/NIF: </label><input type="text" v-model="teacher.dni"/></div>
        <div><label>Materias: </label><input type="text" v-model="subject"/><button @click="handleSubject()">Agregar</button></div>
        <div>
            <ul>
                <li v-for="(item, index) in teacher.subjects" v-bind:key="index">
                    {{ item }}
                </li>
            </ul>
        </div>
        <input type="checkbox" v-model="teacher.doc"/> Documentacion entregada
        <button @click="handleTeacher()">Agregar</button>
    </section>
        <h3>Listado de profesores</h3>
        <table>
            <tr>
                <th>Nombre </th>
                <th>Apellidos </th>
                <th>DNI / NIF </th>
                <th>Materias </th>
                <th>Documentacion entregada </th>
                
            </tr>
            <tr v-for="elm in teachers" :key="elm.dni">
                <th>{{ elm.teachername }}</th>
                <th>{{ elm.surname }}</th>
                <th>{{ elm.dni }}</th>
                <th>
                    <ul>
                        <li v-for="(elm, index) in elm.subjects" :key="index">
                            {{ elm }}
                        </li>
                    </ul>
                </th>
                <th v-if="elm.doc">Entregada</th>
                <th v-else>No entregada</th>
            </tr>
        </table>
    <section>
        
    </section>
</div>
</template>
  
<script lang="ts" setup>
    import {Ref,ref} from 'vue'
    interface ITeacher {
        teachername: string,
        surname: string,
        dni: string
        subjects: Array <string>,
        doc: boolean
    }
    let teacher:Ref<ITeacher>= ref({
        teachername:'',
        surname:'',
        dni:'',
        subjects:[],
        doc: false
    })

    let teachers:Ref<Array<ITeacher>>=ref([])

    let subject:Ref<string>=ref('')
    const handleSubject =() => {
        teacher.value.subjects.push(subject.value)
        subject.value=""
    }

    const handleTeacher =() => {
        teachers.value.push({
            teachername: teacher.value.teachername,
            surname: teacher.value.surname,
            dni:teacher.value.dni,
            subjects:teacher.value.subjects,
            doc:teacher.value.doc
        })
        teacher.value.teachername=''
        teacher.value.surname=''
        teacher.value.dni=''
        teacher.value.subjects=[]
        teacher.value.doc= false
    }
</script>
  
<style scoped>
</style>
  