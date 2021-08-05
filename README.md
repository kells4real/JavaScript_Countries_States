# JavaScript_Countries_States
Javascript json for countries and states.
### For example, in vue you could use a computed property to filter states based on the country selected.

```javascript
data(){
   return { 
   country: "",
   state: ""     
   }
}
computed:{
states() {
        return this.states_item[this.country];
    },
    }
```
With this, whatever country is selected, the state is displayed accordingly.
