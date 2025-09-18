<template>
  <footer>
    <div class="max-w-[1320px] px-4 mx-auto w-full py-11 md:py-16">
      <div
        class="flex items-start lg:flex-row flex-col lg:justify-between gap-8 w-full"
      >
        <!-- Company Branding & Social Media -->
        <div class="space-y-6 max-w-[282px]">
          <!-- Logo -->
          <div
            class="flex items-center gap-2 text-septenary text-[28px] font-semibold font-poppins"
          >
            <img src="/assets/icons/logo.svg" alt="logo" class="size-12" />
            Salty Paws
          </div>

          <!-- Tagline -->
          <p class="text-septenary text-lg font-normal font-sf-pro-display">
            We treat every dog like part of our family, creating a safe, caring,
            and stimulating environment that supports both their physical health
            and emotional well-being.
          </p>

          <!-- Social Media -->
          <div class="flex space-x-3">
            <a
              href="#"
              target="_blank"
              class="size-14 social-media-icon bg-septenary/5 rounded-full flex items-center justify-center hover:bg-septenary/10 transition-colors duration-300"
            >
              <svg
                class="m-auto"
                width="19"
                height="18"
                viewBox="0 0 19 18"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M18.9681 1.33141L15.5077 15.6511C15.3449 16.3256 14.5917 16.673 13.9743 16.3528L9.59796 14.0843L7.52852 17.4837C6.96536 18.4102 5.5405 18.0082 5.5405 16.9251V13.1374C5.5405 12.8444 5.66263 12.5651 5.87297 12.3607L14.4018 4.18582C14.395 4.08364 14.2864 3.99507 14.1779 4.07001L4.0003 11.1822L0.58064 9.41096C-0.219994 8.9954 -0.186069 7.83047 0.641706 7.46941L17.5025 0.0915515C18.3099 -0.262695 19.1784 0.466235 18.9681 1.33141Z"
                  fill="#AF4C0F"
                />
              </svg>
            </a>
            <a
              href="#"
              target="_blank"
              class="size-14 social-media-icon bg-septenary/5 rounded-full flex items-center justify-center hover:bg-septenary/10 transition-colors duration-300"
            >
              <svg
                class="m-auto"
                width="10"
                height="18"
                viewBox="0 0 10 18"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7.99813 2.98875H9.64138V0.12675C9.35788 0.08775 8.38288 0 7.24738 0C4.87813 0 3.25513 1.49025 3.25513 4.22925V6.75H0.640625V9.9495H3.25513V18H6.46063V9.95025H8.96938L9.36763 6.75075H6.45988V4.5465C6.46063 3.62175 6.70963 2.98875 7.99813 2.98875Z"
                  fill="#AF4C0F"
                />
              </svg>
            </a>
            <a
              href="#"
              target="_blank"
              class="size-14 social-media-icon bg-septenary/5 rounded-full flex items-center justify-center hover:bg-septenary/10 transition-colors duration-300"
            >
              <svg
                class="m-auto"
                width="18"
                height="18"
                viewBox="0 0 18 18"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g clip-path="url(#clip0_190_2561)">
                  <path
                    d="M17.982 5.29205C17.9398 4.33564 17.7852 3.67812 17.5636 3.10836C17.3351 2.50359 16.9834 1.96213 16.5227 1.51201C16.0726 1.05489 15.5276 0.699691 14.9298 0.474702C14.3568 0.253147 13.7027 0.0984842 12.7463 0.0563159C11.7827 0.0105764 11.4768 0 9.033 0C6.58916 0 6.28327 0.0105764 5.32329 0.0527447C4.36688 0.0949129 3.70936 0.249713 3.13975 0.471131C2.53483 0.699691 1.99338 1.05132 1.54326 1.51201C1.08614 1.96213 0.731077 2.50716 0.505951 3.10493C0.284397 3.67812 0.129734 4.33207 0.0875658 5.28848C0.0418264 6.25203 0.03125 6.55792 0.03125 9.00176C0.03125 11.4456 0.0418264 11.7515 0.0839946 12.7115C0.126163 13.6679 0.280963 14.3254 0.502518 14.8952C0.731077 15.4999 1.08614 16.0414 1.54326 16.4915C1.99338 16.9486 2.5384 17.3038 3.13618 17.5288C3.70936 17.7504 4.36331 17.905 5.31986 17.9472C6.2797 17.9895 6.58573 17.9999 9.02956 17.9999C11.4734 17.9999 11.7793 17.9895 12.7393 17.9472C13.6957 17.905 14.3532 17.7504 14.9228 17.5288C16.1325 17.0611 17.0889 16.1047 17.5566 14.8952C17.778 14.322 17.9328 13.6679 17.975 12.7115C18.0172 11.7515 18.0277 11.4456 18.0277 9.00176C18.0277 6.55792 18.0242 6.25203 17.982 5.29205ZM16.3611 12.6411C16.3223 13.5202 16.1747 13.9949 16.0516 14.3114C15.7491 15.0956 15.1268 15.7179 14.3426 16.0204C14.0262 16.1434 13.548 16.2911 12.6724 16.3297C11.723 16.372 11.4382 16.3824 9.03657 16.3824C6.6349 16.3824 6.34659 16.372 5.40062 16.3297C4.52155 16.2911 4.04685 16.1434 3.73038 16.0204C3.34015 15.8761 2.98495 15.6476 2.69664 15.3487C2.39775 15.0568 2.16919 14.7052 2.02497 14.315C1.9019 13.9985 1.75424 13.5202 1.71564 12.6447C1.67334 11.6953 1.6629 11.4104 1.6629 9.00876C1.6629 6.60709 1.67334 6.31878 1.71564 5.37295C1.75424 4.49387 1.9019 4.01917 2.02497 3.7027C2.16919 3.31234 2.39775 2.95727 2.70021 2.66883C2.99195 2.36994 3.34358 2.14138 3.73395 1.99729C4.05042 1.87422 4.52869 1.72656 5.40419 1.68783C6.3536 1.64566 6.63847 1.63508 9.04 1.63508C11.4452 1.63508 11.73 1.64566 12.6759 1.68783C13.555 1.72656 14.0297 1.87422 14.3462 1.99729C14.7364 2.14138 15.0916 2.36994 15.3799 2.66883C15.6788 2.96071 15.9074 3.31234 16.0516 3.7027C16.1747 4.01917 16.3223 4.49731 16.3611 5.37295C16.4032 6.32236 16.4138 6.60709 16.4138 9.00876C16.4138 11.4104 16.4032 11.6917 16.3611 12.6411Z"
                    fill="#AF4C0F"
                  />
                  <path
                    d="M9.0341 4.37891C6.48135 4.37891 4.41016 6.44996 4.41016 9.00286C4.41016 11.5558 6.48135 13.6268 9.0341 13.6268C11.587 13.6268 13.6581 11.5558 13.6581 9.00286C13.6581 6.44996 11.587 4.37891 9.0341 4.37891ZM9.0341 12.0023C7.37801 12.0023 6.03466 10.6591 6.03466 9.00286C6.03466 7.34662 7.37801 6.00341 9.0341 6.00341C10.6903 6.00341 12.0335 7.34662 12.0335 9.00286C12.0335 10.6591 10.6903 12.0023 9.0341 12.0023Z"
                    fill="#AF4C0F"
                  />
                  <path
                    d="M14.9208 4.19472C14.9208 4.79084 14.4375 5.2742 13.8412 5.2742C13.2451 5.2742 12.7617 4.79084 12.7617 4.19472C12.7617 3.59845 13.2451 3.11523 13.8412 3.11523C14.4375 3.11523 14.9208 3.59845 14.9208 4.19472Z"
                    fill="#AF4C0F"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_190_2561">
                    <rect width="18" height="18" fill="white" />
                  </clipPath>
                </defs>
              </svg>
            </a>
            <a
              href="#"
              target="_blank"
              class="size-14 social-media-icon bg-septenary/5 rounded-full flex items-center justify-center hover:bg-septenary/10 transition-colors duration-300"
            >
              <svg
                class="m-auto"
                width="19"
                height="18"
                viewBox="0 0 19 18"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M0.04568 0L7.13866 9.48382L0.000976562 17.1946H1.60751L7.85669 10.4436L12.9057 17.1946H18.3724L10.8802 7.17746L17.5239 0H15.9174L10.1624 6.21742L5.5124 0H0.04568ZM2.40816 1.18324H4.91954L16.0096 16.0114H13.4982L2.40816 1.18324Z"
                  fill="#AF4C0F"
                />
              </svg>
            </a>
          </div>
        </div>

        <div
          class="flex items-start sm:flex-row flex-col sm:justify-between gap-4 max-w-[750px] w-full"
        >
          <!-- Overview -->
          <div class="flex flex-col items-start gap-3 max-w-[217px]">
            <h4 class="font-poppins font-semibold text-xl text-septenary">
              Overview
            </h4>
            <ul class="space-y-3 text-xl font-sf-pro-display font-normal">
              <li>
                <a
                  href="#"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Home</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Services</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Coverage area</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >FAQs</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Contact us</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Book us</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Request quote</a
                >
              </li>
            </ul>
          </div>

          <!-- Services -->
          <div class="flex flex-col items-start gap-3 max-w-[134px]">
            <h4 class="font-poppins font-semibold text-xl text-septenary">
              Services
            </h4>
            <ul class="space-y-3 text-xl font-sf-pro-display font-normal">
              <li>
                <a
                  href="/"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Dog Training</a
                >
              </li>
              <li>
                <a
                  href="#about-us"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Dog Boarding</a
                >
              </li>
              <li>
                <a
                  href="#how-we-work"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Dog Daycare</a
                >
              </li>
              <li>
                <a
                  href="#hosting"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Dog Walking</a
                >
              </li>
              <li>
                <a
                  href="#hosting"
                  class="text-septenary hover:text-septenary/50 transition-colors duration-300"
                  >Pet Sitting</a
                >
              </li>
            </ul>
          </div>

          <!-- Contact Us -->
          <div class="flex flex-col items-start gap-3 w-full max-w-[261px]">
            <h4 class="font-poppins font-semibold text-xl text-septenary">
              Get in touch with us
            </h4>
            <div class="space-y-4 text-xl font-sf-pro-display font-normal">
              <a
                href="tel:(+012) - 3456 7890"
                class="flex items-center space-x-3"
              >
                <div>
                  <svg
                    width="21"
                    height="20"
                    viewBox="0 0 21 20"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M5.48288 17.2327L5.81882 17.3932C7.18859 18.1719 8.75457 18.5789 10.3483 18.5704C15.2546 18.5597 19.2858 14.6979 19.2858 10.0087C19.2858 7.74255 18.3441 5.56626 16.6695 3.962C14.9971 2.34116 12.7122 1.42773 10.331 1.42773C5.44705 1.42773 1.42871 5.26875 1.42871 9.93595C1.42871 9.97288 1.42871 10.0093 1.42927 10.0462C1.44398 11.633 1.90835 13.1864 2.77302 14.5411L2.99696 14.8621L2.10114 18.0193L5.48288 17.2327V17.2327Z"
                      fill="#AF4C0F"
                    />
                    <path
                      d="M17.73 2.91904C15.8092 1.0412 13.1742 -0.012287 10.4304 0.000108155H10.4129C4.76223 0.000125089 0.112269 4.45579 0.112269 9.87033C0.112269 9.89573 0.112835 9.9206 0.112835 9.94602C0.134118 11.6675 0.599206 13.3573 1.46671 14.8649L0 20L5.46624 18.6486C6.9763 19.443 8.67396 19.8525 10.3966 19.8378C16.0681 19.8081 20.7175 15.327 20.7141 9.89195C20.7277 7.28061 19.653 4.76929 17.73 2.91904ZM10.4304 18.1622C8.90344 18.1698 7.40337 17.7773 6.09239 17.027L5.75392 16.8649L2.49901 17.6757L3.34517 14.5946L3.11953 14.2703C2.28138 12.9735 1.83733 11.4784 1.8373 9.95303C1.8373 5.4547 5.70034 1.75308 10.3949 1.75308C15.0894 1.75308 18.9524 5.4547 18.9524 9.95303C18.9524 12.7854 17.4209 15.4243 14.9094 16.9189C13.5812 17.7342 12.036 18.1658 10.4586 18.1622M15.4172 12.1622L14.7966 11.8919C14.7966 11.8919 13.894 11.5136 13.3299 11.2433C13.2735 11.2433 13.2171 11.1892 13.1607 11.1892C13.0216 11.1925 12.8857 11.2297 12.7658 11.2973C12.6457 11.3649 12.7094 11.3514 11.9197 12.2162C11.8661 12.3173 11.7561 12.3806 11.6376 12.3784H11.5812C11.4964 12.3648 11.4178 12.3272 11.3556 12.2703L11.0735 12.1622C10.4683 11.9167 9.91415 11.5688 9.43756 11.1352C9.32474 11.0271 9.15552 10.919 9.04268 10.8109C8.62508 10.4275 8.26444 9.99101 7.97089 9.51358L7.91446 9.40547C7.86546 9.3394 7.8274 9.26646 7.80164 9.18925C7.78689 9.09562 7.80685 8.99999 7.85805 8.919C7.90939 8.8379 8.0837 8.64871 8.25293 8.48655C8.42217 8.3244 8.42217 8.2163 8.53499 8.10818C8.59297 8.03102 8.63304 7.94285 8.6525 7.84962C8.67196 7.75638 8.67036 7.66023 8.64781 7.56763C8.38491 6.86821 8.08364 6.18257 7.74524 5.51361C7.65453 5.37844 7.51322 5.28171 7.35036 5.24334H6.72983C6.61701 5.24334 6.5042 5.29739 6.39136 5.29739L6.33496 5.35144C6.22214 5.40549 6.10932 5.51361 5.99649 5.56766C5.88367 5.62171 5.82726 5.78388 5.71444 5.89198C5.32008 6.3695 5.10188 6.95873 5.09392 7.56763C5.10017 7.99596 5.19607 8.41872 5.37596 8.81088L5.43238 8.97303C5.93891 10.0107 6.6473 10.9464 7.5196 11.7298L7.74524 11.946C7.90944 12.0763 8.06053 12.2211 8.19652 12.3784C9.36535 13.353 10.7536 14.0557 12.2525 14.4325C12.4217 14.4865 12.6474 14.4865 12.8166 14.5406H13.3807C13.6755 14.5266 13.9639 14.4529 14.2269 14.3243C14.3651 14.2643 14.4971 14.1919 14.6217 14.1081L14.7346 14C14.8474 13.8919 14.9602 13.8379 15.073 13.7298C15.1833 13.6356 15.2783 13.5263 15.3551 13.4054C15.4634 13.1633 15.5395 12.9092 15.5807 12.6487V12.2703C15.53 12.2267 15.473 12.1903 15.4115 12.1622"
                      fill="#F5F1E8"
                    />
                  </svg>
                </div>

                <span class="text-septenary">(+012) - 3456 7890</span>
              </a>

              <a
                href="tel:(+012) - 3456 7890"
                class="flex items-center space-x-3"
              >
                <div>
                  <svg
                    width="22"
                    height="22"
                    viewBox="0 0 22 22"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <g clip-path="url(#clip0_190_2598)">
                      <path
                        d="M12.879 5.50065C13.7744 5.67534 14.5972 6.11322 15.2422 6.75826C15.8873 7.4033 16.3252 8.22614 16.4999 9.12148M12.879 1.83398C14.7392 2.04063 16.4738 2.87364 17.7981 4.19624C19.1223 5.51884 19.9575 7.25241 20.1665 9.11232M9.37458 12.7085C8.27314 11.607 7.40341 10.3616 6.76542 9.03278C6.71054 8.91848 6.6831 8.86133 6.66202 8.78901C6.58711 8.53202 6.64092 8.21645 6.79676 7.99881C6.84061 7.93756 6.89301 7.88517 6.99779 7.78038C7.31826 7.45991 7.4785 7.29967 7.58326 7.13854C7.97834 6.53089 7.97834 5.74753 7.58326 5.13988C7.4785 4.97875 7.31827 4.81851 6.99779 4.49804L6.81916 4.31941C6.33201 3.83226 6.08843 3.58868 5.82683 3.45636C5.30657 3.19321 4.69216 3.19321 4.17189 3.45636C3.91029 3.58868 3.66671 3.83226 3.17956 4.31941L3.03506 4.46391C2.54957 4.9494 2.30683 5.19214 2.12143 5.52217C1.91572 5.88838 1.7678 6.45717 1.76905 6.87721C1.77018 7.25574 1.84361 7.51444 1.99046 8.03185C2.77968 10.8125 4.26879 13.4363 6.45777 15.6253C8.64675 17.8143 11.2706 19.3034 14.0512 20.0926C14.5686 20.2394 14.8273 20.3129 15.2058 20.314C15.6259 20.3152 16.1947 20.1673 16.5609 19.9616C16.8909 19.7762 17.1336 19.5335 17.6191 19.048L17.7636 18.9035C18.2508 18.4163 18.4944 18.1728 18.6267 17.9112C18.8898 17.3909 18.8898 16.7765 18.6267 16.2562C18.4944 15.9946 18.2508 15.751 17.7636 15.2639L17.585 15.0853C17.2645 14.7648 17.1043 14.6045 16.9432 14.4998C16.3355 14.1047 15.5522 14.1047 14.9445 14.4998C14.7834 14.6045 14.6231 14.7648 14.3027 15.0853C14.1979 15.19 14.1455 15.2424 14.0842 15.2863C13.8666 15.4421 13.551 15.4959 13.294 15.421C13.2217 15.3999 13.1646 15.3725 13.0503 15.3176C11.7215 14.6796 10.476 13.8099 9.37458 12.7085Z"
                        stroke="#AF4C0F"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                    </g>
                    <defs>
                      <clipPath id="clip0_190_2598">
                        <rect width="22" height="22" fill="white" />
                      </clipPath>
                    </defs>
                  </svg>
                </div>

                <span class="text-septenary">(+012) - 3456 7890</span>
              </a>

              <a
                href="mailto:info@example.com"
                class="flex items-center space-x-3"
              >
                <div>
                  <svg
                    width="22"
                    height="22"
                    viewBox="0 0 22 22"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M19.7085 16.4993L13.6192 10.9993M8.38111 10.9993L2.29186 16.4993M1.8335 6.41602L9.318 11.6552C9.92408 12.0794 10.2271 12.2916 10.5567 12.3737C10.8479 12.4463 11.1524 12.4463 11.4436 12.3737C11.7732 12.2916 12.0762 12.0794 12.6823 11.6552L20.1668 6.41602M6.2335 18.3327H15.7668C17.307 18.3327 18.077 18.3327 18.6653 18.033C19.1827 17.7693 19.6034 17.3486 19.8671 16.8312C20.1668 16.2429 20.1668 15.4728 20.1668 13.9327V8.06602C20.1668 6.52587 20.1668 5.7558 19.8671 5.16754C19.6034 4.6501 19.1827 4.2294 18.6653 3.96575C18.077 3.66602 17.307 3.66602 15.7668 3.66602H6.2335C4.69335 3.66602 3.92328 3.66602 3.33502 3.96575C2.81758 4.2294 2.39688 4.6501 2.13323 5.16754C1.8335 5.7558 1.8335 6.52587 1.8335 8.06602V13.9327C1.8335 15.4728 1.8335 16.2429 2.13323 16.8312C2.39688 17.3486 2.81758 17.7693 3.33502 18.033C3.92328 18.3327 4.69335 18.3327 6.2335 18.3327Z"
                      stroke="#AF4C0F"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </div>

                <span class="text-septenary">saltypawsericeira@gmail.com</span>
              </a>

              <div class="flex items-start space-x-3">
                <div>
                  <svg
                    width="18"
                    height="22"
                    viewBox="0 0 18 22"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M8.99984 11.459C10.5186 11.459 11.7498 10.2278 11.7498 8.70898C11.7498 7.1902 10.5186 5.95898 8.99984 5.95898C7.48105 5.95898 6.24984 7.1902 6.24984 8.70898C6.24984 10.2278 7.48105 11.459 8.99984 11.459Z"
                      stroke="#AF4C0F"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      d="M8.99984 20.1673C10.8332 16.5007 16.3332 14.1341 16.3332 9.16732C16.3332 5.11723 13.0499 1.83398 8.99984 1.83398C4.94975 1.83398 1.6665 5.11723 1.6665 9.16732C1.6665 14.1341 7.1665 16.5007 8.99984 20.1673Z"
                      stroke="#AF4C0F"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </div>

                <span class="text-septenary">
                  SaltyPaws Ericeira - Mafra e Sintra Lisbon 2640, Portugal.
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Section - Copyright & Legal -->
    <div
      class="max-w-[1320px] px-4 mx-auto py-6 border-t border-septenary w-full"
    >
      <div
        class="flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0"
      >
        <div class="text-septenary text-lg font-sf-pro-display font-normal">
          © 2025 Salty Paws. All rights reserved.
        </div>
        <div class="flex items-center space-x-4">
          <a
            href="#"
            class="text-septenary text-sm sm:text-lg font-sf-pro-display font-normal hover:text-septenary/50 transition-colors duration-300"
            >Term of use</a
          >
          <div
            class="text-[#A0A4AD] border border-[#A0A4AD] w-[0.5px] h-[20px]"
          ></div>
          <a
            href="#"
            class="text-septenary text-sm sm:text-lg font-sf-pro-display font-normal hover:text-septenary/50 transition-colors duration-300"
            >Privacy Policy</a
          >
          <div
            class="text-[#A0A4AD] border border-[#A0A4AD] w-[0.5px] h-[20px]"
          ></div>
          <a
            href="#"
            class="text-septenary text-sm sm:text-lg font-sf-pro-display font-normal hover:text-septenary/50 transition-colors duration-300"
            >Cancellation policy</a
          >
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.social-media-icon {
  backdrop-filter: blur(25px);
}
</style>