# JavaScript_Countries_States
Javascript json for countries and states.
### For example, in vue you could use a computed hook to filter states based on the country selected.

```javascript
data(){
   return { 
   // countries: country_items from the json.js file
   // states_item: states_item from the json.js file
   country: "",
   state: ""     
   }
},
computed:{
states() {
        return this.states_item[this.country];
    }
    },
```

With this, whatever country is selected, the state is displayed accordingly.

If you wanted to post the info to a backend for example, you could do this:
```javascript
 // Always use an async function for retreiving or posting data 
 methods: {
 async def postInfo(){
     let data = { country : this.country,
                  state : this.state }
     url = 'api/user-data/'
     const response = await axios.post(url, data);
     if (response){
        // Do what ever you want  
     }
  }
  }
```
In your template, you should loop over countries and states as thus

```html
<template>
   <label>Country</label>
   <select>
    <option v-for="item in country_items" :key="item">
      {{item}}
    </option>
   </select>
   
   <label>State</label> 
    <option v-for="item in states" :key="item">
      {{item}}
    </option>
</template>

```
You can even make this into a reuseable component

This logic can be applied to react, Angular or any other JS frontend framework



