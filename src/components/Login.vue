<template>
    <div>
        <div class="main">

             <h1>MY MILL</h1>

            <form>
                
                        <label for="email">e-mail</label><br/>
                        <div>
                            <input type="email" name="" id="email" placeholder="Enter email" required v-model="email"><br/>
                        </div><br/>
                        
                        <label for="password">password</label><br/>
                        <div class="passdiv">
                            <input :type="state? `password` : `text`" name="" id="password" placeholder="Enter password" required v-model="password"><span><img src="../assets/icons/eye.svg" id="eye" v-on:click="show()" alt=""></span>
                            
                            
                        </div>
                        <p>Forgot password?<a href="#" id="recover">Recover here</a><img src="../assets/icons/lock.svg" id="lock" alt=""></p>
                        
                        
                        <p><input type="checkbox" :checked="true" name="terms" id="mark">I agree to the <a href="#">TERMS AND CONDITIONS</a></p>
                        
                        <button>log in</button>

                   
                  
            </form>
            
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
        password: "",
        email: "",  
        state: true,
        }
        
    },
    methods: {
      show(){
          this.state = !this.state
         }  
    }
}
</script>

<style scoped>
    h1 {
  color: #173f5f;
}

.main {
  max-width: 40rem;
  font-family: 'Montserrat', sans-serif;
  background-color: #fff;
  margin:5rem auto;
  padding: 2% 5%;
}
form {
  max-width: 25rem;
  margin: auto;
}
form label {
  text-transform: uppercase;
  font-weight: bold;
  font-size: 1.1rem;
  color: #244a6f;
  }

form input {
  margin-top: 1rem;
  padding: 10px 14px 2px 14px;
  border: none;
  border-bottom: 2px solid #244a6f;
  background: #eff4fa;
  font-size: 1rem;
}

form p {
  color: #929292;
  text-align: center;
}
form button {
  text-transform: uppercase;
  display: block;
  width: 70%;
  padding: 1rem 1.5rem;
  margin: 0 auto;
  font-weight: bold;
  color: #fff;
  background-image: linear-gradient(to right, #244a6f, #20639b);
  border-style: none;
  border-radius: 6px;
}

form a {
  text-decoration: none;
  color: #929292;
}

.passdiv {
  width: 100%;
  position: relative;
}
.passdiv input,#email {
  width: 100%;
}

span {
  position: absolute;
  right: 1rem;
  top: 43%;
  cursor: pointer;
}

#mark {
  margin: 0 0.5rem;
  appearance: none;
  background-color: #fefeff;
  height: 14px;
  width: 14px;
  padding: inherit;
  border-radius: 2px;
  border: 1px solid #244a6f;
}
#mark:checked {
  background-color: #244a6f;
}

#lock {
  margin: 1rem 0.7rem 0 ;
}
#recover{
    text-decoration: underline;
}



</style>