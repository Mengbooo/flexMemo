<template>
 <div class="main-container">
        <div class="login-box">
            <div class="logo">
                <img src="./assets/imgs/logo.png" alt="">
            </div>
            <div class="form">
                <form action="#">
                    <input type="text" placeholder="username">
                    <input type="password" placeholder="password">
                    <button type="submit">login / register</button>
                </form>
            </div>
        </div>
        <div class="border">
            <div class="slogan">
                hope you have a good day
            </div>
        </div>
    </div>
</template>


<script setup>


</script>


<style scoped lang="less">
.main-container {
    width: 100dvw;
    height: 100dvh;
    display: flex;
    align-items: center;

    .login-box {
        width: 50%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        .logo {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 5%;
            img {
                width: 18%;
            }
        }

        .form {
            width: 100%;
            form {
                width: 100%;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                input{
                    margin: 2% 0;
                    border-color: rgb(79, 255, 120);
                    border-style: solid;
                    border-radius: 20px;
                    font-family:Georgia, 'Times New Roman', Times, serif;
                    width: 50%;
                    height: 5dvh;
                    text-align:center
                }
                input:focus{
                    border-color: #ffffff;
                }
                button {
                    margin-top: 2%;
                    width: 40%;
                    height: 5dvh;
                    border-radius: 12px;
                    border: none;
                    color: rgb(255, 255, 255);
                    font-family: Georgia, 'Times New Roman', Times, serif;
                    background-color: #7f7f7f77;
                    transition: all 0.3s ease-in-out;
                    cursor: pointer;
                }
                button:hover{
                    background-color: #00711a;
                    transition: all 0.3s ease-in-out;
                }
            }

        }
    }

    .border {
        width: 50%;
        height: 100%;
        background: linear-gradient(45deg, #09a416, #0172af);
        display: flex;
        justify-content: center;
        align-items: center;

        .slogan {
            font-family: mono;
            font-size: 2.5dvw;
            font-weight: 600;
            color: rgb(37, 37, 37);
        }
    }

}
</style>