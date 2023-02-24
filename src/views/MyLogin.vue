<template>
    <div class ="login-container">
        <div class="login-box">
            
            <div class="text-center avatar-box">
                <img src="../assets/logo.svg" class="img-thumbnail avatar" alt="" width="200">
            </div>

            <div class="form-login p-4">
                <div class="form-group form-inline">
                    <label for="username"> name </label>
                    <input type="text" class="form-control ml-2" id="username" placeholder="please input login name" autocomplete="off"
                    v-model.trim="username">
                </div>
            </div>

            <div class="form-group form-inline">
                <label for="password">password</label>
                <input type="password" class="form-control ml-2" id="password" placeholder="please input password"
                v-model.trim="password" @keyup.enter="onLoginClick($event)">
                <!--@keyup.一个键 当key是该键的时候调用事件-->
            </div>
            <div class="form-group form-inline d-flex justify-content-end">
                <button type="button" class="btn btn-secondary mr-2" @click="clearInput">reset</button>
                <button type="button" class="btn btn-primary" @click="onLoginClick($event)">login</button>
                <!--onLoginClick($event)可以使用两个参数➡onLoginClick(step，$event) step是一个单纯传值 使用step接收，
                    1$event是原生的事件参数对象 比如说在这个环境下就是一个按钮按下的动作-->
                <h3>count:{{ count }}</h3>
                <button @click="count+=1">+1</button>
                <!--v-on可以简写成为@,同时简单的命令可以直接写在@click中-->
            </div>


        </div>
    </div>
</template>

<script>

export default ({
    name: 'MyLogin',
    data(){
        return{
        username:'',
        password:'',
        count: 0
    }
    },
    methods:{
        onLoginClick(e){
            
            if(this.username === 'admin' && this.password === '123456'){
                this.$router.push('/')
                localStorage.setItem('token', 'Bearer xxx')
            }else{
                localStorage.removeItem('token')
                const nowBgcolor = e.target.style.backgroundColor
                console.log(nowBgcolor)
                e.target.style.backgroundColor = nowBgcolor === 'red' ? 'red' : 'red'
            }
        },
        clearInput(e){
            this.username=''
            this.password=''

        }
    }
    
})
</script>



