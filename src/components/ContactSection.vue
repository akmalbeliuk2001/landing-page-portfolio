<template>
  <div class="bg-[#000] h-screen w-full">
    <div class="relative mx-4 md:mx-7 lg:mx-auto lg:max-w-[1064px] h-full">
      <div
        class="absolute left-[50%] translate-x-[-50%] top-[50%] translate-y-[-50%] w-full"
      >
        <p
          class="poppins font-semibold text-[#F44F1A] text-[48.8px] lg:text-[76.29px] -tracking-widest mb-8"
        >
          CONTACT
        </p>
        <div
          class="flex justify-between items-center py-2 border-solid border-b-[1px] border-[#fff] mb-4"
        >
          <P
            class="poppins text-[#fff] font-semibold text-[25px] lg:text-[48.83px] -tracking-widest"
            >INSTAGRAM</P
          >
          <a href="https://www.instagram.com/akmal_beliuk/" target="_blank">
            <div
              class="more flex items-center px-4 py-2 border-solid border-[1px] border-[#fff] rounded-[30px] w-max"
            >
              <p
                class="poppins font-normal text-[16px] lg:text-[20px] text-[#fff] mr-2"
              >
                SEE
              </p>
            </div>
          </a>
        </div>
        <div
          class="flex justify-between items-center py-2 border-solid border-b-[1px] border-[#fff] mb-4"
        >
          <P
            class="poppins text-[#fff] font-semibold text-[25px] lg:text-[48.83px] -tracking-widest"
            >LINKEDIN</P
          >
          <a
            href="https://www.linkedin.com/in/muhammad-akmal-beliuk-168068223/"
            target="_blank"
          >
            <div
              class="more flex items-center px-4 py-2 border-solid border-[1px] border-[#fff] rounded-[30px] w-max"
            >
              <p
                class="poppins font-normal text-[16px] lg:text-[20px] text-[#fff] mr-2"
              >
                SEE
              </p>
            </div>
          </a>
        </div>
        <div
          class="flex justify-between items-center py-2 border-solid border-b-[1px] border-[#fff] mb-4"
        >
          <P
            class="poppins text-[#fff] font-semibold text-[25px] lg:text-[48.83px] -tracking-widest"
            >GITHUB</P
          >
          <a href="https://github.com/akmalbeliuk2001" target="_blank">
            <div
              class="more flex items-center px-4 py-2 border-solid border-[1px] border-[#fff] rounded-[30px] w-max"
            >
              <p
                class="poppins font-normal text-[16px] lg:text-[20px] text-[#fff] mr-2"
              >
                SEE
              </p>
            </div>
          </a>
        </div>
        <div
          class="flex justify-between items-center py-2 border-solid border-b-[1px] border-[#fff]"
        >
          <P
            class="poppins text-[#fff] font-semibold text-[25px] lg:text-[48.83px] -tracking-widest"
            >EMAIL</P
          >
          <p
            id="email"
            type="text"
            value="akmalbeliuk@gmail.com"
            :class="
              copied
                ? 'border-[#F44F1A] bg-[#F44F1A] text-[#000]'
                : 'border-[#fff] text-[#fff]'
            "
            class="poppins font-normal text-[16px] lg:text-[20px] px-4 py-2 border-solid border-[1px] rounded-[30px] w-max cursor-pointer hover:border-[#F44F1A] hover:bg-[#F44F1A] hover:text-[#000]"
            @click="copyClipboard()"
          >
            {{ email }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const email = ref("akmalbeliuk@gmail.com");
const copied = ref(false);

const copyClipboard = () => {
  const emailElement = document.getElementById("email");
  navigator.clipboard.writeText(emailElement.textContent);
  email.value = "Copied!";
  copied.value = true;
  setTimeout(() => {
    email.value = "akmalbeliuk@gmail.com";
    copied.value = false;
  }, 1000);
};
</script>

<style lang="scss" scoped>
.more {
  transition: all 0.3s ease-in;
  p::after {
    content: url("@/assets/white_arrow.png");
    margin-left: 8px;
    width: 17.89px;
  }
}
.more:hover {
  background-color: #f44f1a;
  border-color: #f44f1a;
  p {
    color: #000;
  }
  p::after {
    content: url("@/assets/black_arrow.png");
    margin-left: 8px;
    width: 17.89px;
  }
}
</style>
