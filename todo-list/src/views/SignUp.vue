<template>
  <form @submit.prevent="handleSubmit">
    <div class="container">
      <h1>SIGN UP</h1>
      <br />
      <div class="container1">
        <div class="row">
          <div class="col-md-3"></div>
          <div class="col-md-6">
            <form>
              <div class="mb-3">
                <label for="exampleInputEmail1" class="form-label">Email</label>
                <input
                  type="email"
                  v-model="email"
                  class="form-control"
                  id="exampleInputEmail1"
                  aria-describedby="emailHelp"
                />
                <div id="emailHelp" class="form-text" style="font-size: 8.5px">
                  We'll never share your email with anyone else.
                </div>
              </div>
              <div class="mb-3">
                <label for="exampleInputPassword1" class="form-label"
                  >Password</label
                >
                <input
                  type="password"
                  v-model="password"
                  class="form-control"
                  id="exampleInputPassword1"
                />
                <br />
                <label for="exampleInputPassword1" class="form-label"
                  >Password</label
                >
                <input
                  type="password"
                  v-model="password_confirmation"
                  class="form-control"
                  id="exampleInputPassword1"
                />
                <hr />
              </div>
              <div class="btnSign">
                <router-link to="/signin">
                <button type="submit" class="btnSignIn">Sign Up</button>
                </router-link>
                <br />
                <router-link to="/signin">
                <button type="submit" class="btnSignUp">Sign In</button>
                </router-link>
              </div>
            </form>
          </div>
          <div class="linker">Copyright @2019</div>
        </div>
      </div>
    </div>
  </form>
</template>

<script>
/* import axios from 'axios'
export default {
  name: "SignUp",
  data() {
    return {
      email: "",
      password: "",
      password_confirmation: "",
    };
  },
  methods: {
    handleSubmit() {
      const data = {
        email: this.email,
        password: this.password,
        password_confirmation: this.password_confirmation,
      };
      axios.post('http://localhost:8080/#/signup', data)
      .then(res => {
        console.log(res)
      }
      ).catch(err => {
        console.log(err)
      })
    },
  },
}; */
import {reactive} from 'vue';
import {useRouter} from "vue-router";
export default {
  name: "SignUp",
  setup() {
    const data = reactive({
      email: '',
      password: '',
      password_confirmation: "",
    });
    const router = useRouter();
    const submit = async () => {
      await fetch('https://mockup-api.herokuapp.com/auth/signup', {
        method: 'POST',
        headers: {'Content-Type': 'application/json'},
        body: JSON.stringify(data)
      });
      await router.push('/signin');
    }
    return {
      data,
      submit
    }
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  font-weight: 900;
}
.container {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  padding-top: 100px;
  background-color: rgb(221, 233, 241);
}
.container1 {
  background: white;
  padding: 30px 0 50px 0;
  width: 400px;
  margin: auto;
}
.btnSign {
  text-align: center;
  text-decoration: none;
}
.btnSignIn {
  margin-left: 0px;
  margin-top: 12px;
  border-top-right-radius: 10px;
  border-bottom-left-radius: 10px;
  border-top-left-radius: 10px;
  border-bottom-right-radius: 10px;
  border: none #ffff;
  background: rgb(25, 235, 130);
  width: 100%;
  font-size: 16px;
  padding-top: 3px;
  padding-bottom: 3px;
}
.btnSignUp {
  margin-top: 12px;
  border-top-right-radius: 10px;
  border-bottom-left-radius: 10px;
  border-top-left-radius: 10px;
  border-bottom-right-radius: 10px;
  border: none #ffff;
  width: 100%;
  font-size: 16px;
  padding-top: 3px;
  padding-bottom: 3px;
}
.linker {
  padding-top: 12px;
  text-align: center;
}
hr {
  border-bottom: 2px solid rgb(229, 233, 29);
  line-height: 0.1em;
  margin: 20px 0 10px;
}
</style>
