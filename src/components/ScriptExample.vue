<template>
    <div>
        <p></p>
        <p></p>
        <p></p>
    </div>
</template>

<!-- each key value is one of your variables -->
<!-- usually life cycle hooks you keep it simple as possible and CALL FUNCTIONS, not write functions in them -->
<script>
    export default {
        name : "ScriptExample",
        data() {
            return {
                tweets : ["M-o-o-n, that spells I Love You", "Tweet 2", "Tweet 3"],
                numFriends : 50,
                isLoggedIn : true,
            }
        },
        methods: {
            showInfo() {
                console.log("ShowInfo");
                const myDiv = document.querySelector(`div`);
                myDiv.insertAdjacentHTML('beforeend', `<h2>${this.numFriends}</h2>`);
                // TERNARY OPERATOR OTHER WAY TO DO CONDITION BASED ONLY WORKS WITH TRUE OR FALSE 2 CONDITIONS
                myDiv.insertAdjacentHTML(`beforeend`, `<h3>${this.isLoggedIn? "Welcome to the page!" : "User is not logged in."}`);
                    // the Ternary Operator is equivalent to the if statement below:
                // if(this.isLoggedIn){
                //     myDiv.insertAdjacentHTML('beforeend', `<h3>Welcome to the page.</h3>`);
                // }else{
                //     myDiv.insertAdjacentHTML('beforeend', `<h3>User is not logged in.</h3>`);
                // }
                for (let tweet of this.tweets){
                    myDiv.insertAdjacentHTML(`beforeend`, `<p>${tweet}</p>`)
                }
            }
        },
        mounted () {
            this.showInfo();
        },
    }
</script>

<style scoped>

</style>