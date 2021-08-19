<template>
        <div>
                <h1>Eventhandling component</h1><hr />
                <!-- <h2>{{ name }}</h2>
                <button v-on:click="name ='Lonikar'">Sir Name</button> 
                <div>
                        <h2>{{ count }}</h2>
                        <button v-on:click="count +=1">Increment</button>
                        <button v-on:click="count -=1">Increment</button>
                </div><hr /> -->

                <div>
                        <pre>
                                {{ JSON.stringify(formValues, null, 2)}}
                        </pre>
                </div>

                <form @submit="submitForm">
                        <div>
                           <label for="name">Name</label>
                           <input type="text" id="name" v-model.trim="formValues.name">
                        </div>
                        <div>
                           <label for="profile">Profile Summary</label>
                           <textarea  id="profile" v-model="formValues.profileSummary" />
                        </div>

                        <div>
                                <label for="country"> Country</label>
                                <select id="country" v-model="formValues.country">
                                        <option value="">Selecte Country</option>
                                        <option value="india">India</option>
                                        <option value="Vietname">Vietnam</option>
                                        <option value="singapore">Singapore</option>
                                </select>
                        </div>

                        <div> 
                                <label for="joblocation"> Country</label>
                                <select id="joblocation" multiple v-model="formValues.joblocation">
                                       
                                        <option value="india">India</option>
                                        <option value="Vietname">Vietnam</option>
                                        <option value="singapore">Singapore</option>
                                </select>
                        </div>

                        <div>
                          <input type="checkbox"
                           id="remoteWork"
                           v-model="formValues.remoteWork" 
                           true-value="yes"
                           false-value="no"
                           />
                          <label for="remoteWork">Open to remote work</label>
                        </div>
                        <div>
                           <label>Skill Set</label>
                           <input type="checkbox" id="html" value="html" v-model="formValues.skillSet" />  
                           <label for="skillSet">HTML & CSS</label>  
                           <input type="checkbox" id="js" value="js"  v-model="formValues.skillSet" />  
                           <label for="skillSet">JavaScrip</label>  
                           <input type="checkbox" id="vuejs" value="vuejs" v-model="formValues.skillSet" />  
                           <label for="skillSet">VueJs</label>   
                        </div>
                        <div>
                                <label>Years of Experience</label>
                                <input type="radio"
                                 id="0-2"
                                 value="0-2"
                                 v-model="formValues.yearsOfExperience" 
                                 />
                                <label for="0-2">0-2</label>

                                <input type="radio" id='3-5' value="3-5" v-model="formValues.yearsOfExperience" />
                                <label for="3-5">3-5</label>

                                <input type="radio" id='6-10' value="6-10" v-model="formValues.yearsOfExperience" />
                                <label for="6-10">6-10</label>

                                <input type="radio" id='10+' value="10+" v-model="formValues.yearsOfExperience" />
                                <label for="10+">10+</label>
                        </div>
                        <div>
                                <button>Submit</button>
                        </div>
                </form>

        </div>
</template>

<script>
export default {
        name: 'Eventhandling',
        data() {
                return{
                        // name: 'Rakesh',
                        // count: 0,
                        formValues: {
                                name: '',
                                profileSummary: '',
                                country: '',
                                joblocation: [],
                                remoteWork: "no",
                                skillSet: [],
                                yearsOfExperience: '',
                           
                        }
                        
                }
        },
        methods: {
                submitForm(event) {
                        event.preventDefault()
                        console.log('Form values', this.formValues)
                }
        },
       
}
       
</script>

<style scoped>
label {
        font-weight: bold;
        display: flex;
        margin-bottom: 5px;
}
input + label {
        font-weight: bold;
        display: inline-flex;
        margin-right: 20px;
}
input[type='text'],
textarea,
select {
        display: block;
        width: 400px;
        padding: 6px 12px;
        font-size: 14px;
        line-height: 1.42857143;
        color: #555;
        background-color: #fff;
        background-image: none;
        border: 1px solid #ccc;
        border-radius: 4px;
}

</style>