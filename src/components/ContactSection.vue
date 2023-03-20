<template>
  <div class="bg-[#000] h-screen w-full">
    <div class="relative mx-auto px-4 md:px-7 lg:px-0 lg:max-w-[1064px] h-full">
      <div class="absolute left-[50%] translate-x-[-50%] top-[50%] translate-y-[-50%] w-full">
        <p class="poppins font-semibold text-[#F44F1A] text-[76.29px] -tracking-widest mb-8">CONTACT</p>
        <div class="flex justify-between items-center px-2 border-solid border-b-[1px] border-[#fff] mb-4">
          <P class="poppins text-[#fff] font-semibold text-[48.83px] -tracking-widest">INSTAGRAM</P>
          <a href="">
            <div class="more flex items-center px-4 py-2 border-solid border-[1px] border-[#fff] rounded-[30px] w-max">
              <p class="poppins font-normal text-[20px] text-[#fff] mr-2">SEE</p>  
            </div>
          </a>
        </div>
        <div class="flex justify-between items-center px-2 border-solid border-b-[1px] border-[#fff] mb-4">
          <P class="poppins text-[#fff] font-semibold text-[48.83px] -tracking-widest">LINKEDIN</P>
          <a href="">
            <div class="more flex items-center px-4 py-2 border-solid border-[1px] border-[#fff] rounded-[30px] w-max">
              <p class="poppins font-normal text-[20px] text-[#fff] mr-2">SEE</p> 
            </div>
          </a>
        </div>
        <div class="flex justify-between items-center px-2 border-solid border-b-[1px] border-[#fff] mb-4">
          <P class="poppins text-[#fff] font-semibold text-[48.83px] -tracking-widest">GITHUB</P>
          <a href="">
            <div class="more flex items-center px-4 py-2 border-solid border-[1px] border-[#fff] rounded-[30px] w-max">
              <p class="poppins font-normal text-[20px] text-[#fff] mr-2">SEE</p> 
            </div>
          </a>
        </div>
        <div class="flex justify-between items-center px-2 border-solid border-b-[1px] border-[#fff]">
          <P class="poppins text-[#fff] font-semibold text-[48.83px] -tracking-widest">EMAIL</P>
          <p class="poppins font-normal text-[20px] text-[#fff] px-4 py-2 border-solid border-[1px] border-[#fff] rounded-[30px] w-max">akmalbeliuk@gmail.com</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style lang="scss" scoped>
.more {
  transition: all .3s ease-in;
  p::after {
    content: url('@/assets/white_arrow.png');
    margin-left: 8px;
    width: 17.89px;
  }
}
.more:hover {
  background-color: #F44F1A;
  border-color: #F44F1A;
  p {
    color: #000;
  }
  p::after {
    content: url('@/assets/black_arrow.png');
    margin-left: 8px;
    width: 17.89px;
  }
}
</style>