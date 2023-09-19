<template>
  <div class="container">
    <div class="calculator">
      <input ref="inputBox" type="text" placeholder="0" />
      <div>
        <button class="button operator">AC</button>
        <button class="button operator">DEL</button>
        <button class="button operator">%</button>
        <button class="button operator">/</button>
      </div>
      <div>
        <button class="button">7</button>
        <button class="button">8</button>
        <button class="button">9</button>
        <button class="button operator">*</button>
      </div>
      <div>
        <button class="button">4</button>
        <button class="button">5</button>
        <button class="button">6</button>
        <button class="button operator">-</button>
      </div>
      <div>
        <button class="button">1</button>
        <button class="button">2</button>
        <button class="button">3</button>
        <button class="button operator">+</button>
      </div>
      <div>
        <button class="button">00</button>
        <button class="button">0</button>
        <button class="button">.</button>
        <button class="button equalBtn">=</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    let input = this.$refs.inputBox;
    let buttons = this.$el.querySelectorAll('button');

    let string = "";
    let arr = Array.from(buttons);
    arr.forEach(button => {
      button.addEventListener('click', (e) => {
        if (e.target.innerHTML === '=') {
          string = eval(string);
          input.value = string;
        } else if (e.target.innerHTML === 'AC') {
          string = "";
          input.value = string;
        } else if (e.target.innerHTML === 'DEL') {
          string = string.substring(0, string.length - 1);
          input.value = string;
        } else {
          string += e.target.innerHTML;
          input.value = string;
        }
      });
    });
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body{
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(45deg, #0a0a0a, #3a4452);
}

.calculator{
    border: 1px solid #717377;
    padding: 20px;
    border-radius: 16px;
    background: transparent;
    box-shadow: 0px 3px 15px rgba(113, 115, 119, 0.5);

}

input{
    width: 320px;
    border: none;
    padding: 24px;
    margin: 10px;
    background: transparent;
    box-shadow: 0px 3px 15px rgbs(84, 84, 84, 0.1);
    font-size: 40px;
    text-align: right;
    cursor: pointer;
    color: #ffffff;
}

input::placeholder{
    color: #ffffff;
}

button{
    border: none;
    width: 60px;
    height: 60px;
    margin: 10px;
    border-radius: 50%;
    background: transparent;
    color: #ffffff;
    font-size: 20px;
    box-shadow: -8px -8px 15px rgba(255, 255, 255, 0.1);
    cursor: pointer;
}

.equalBtn{
    background-color: #fb7c14;
}

.operator{
    color: #6dee0a;
}
</style>
