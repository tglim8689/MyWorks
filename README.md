# DGIST Works
Recently works

- 20200909 : Ver 0.22
  - No crystal : 16MHz 동작 ==> 8MHz external Xtal 적용 : 180 MHz 동작
    - system_stm32f4xx.c : 
      #define PLL_M      5      // org=25
      #define PLL_N      225    // org=360
      
    - stm32f4xx.h : 
      //  #define HSE_VALUE    ((uint32_t)25000000)
      #define HSE_VALUE    ((uint32_t)8000000)

  - 16MHz 에서 FFT(1024) 500msec ==> 18MHz 변경 후 FFT(1024) 60msec
