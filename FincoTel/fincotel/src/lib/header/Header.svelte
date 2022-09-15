<script>
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
  import fincotel from "$lib/assets/fincotel.png"
  import mobnav from "$lib/mobile-nav/MobNav.svelte"
  import Link from '$lib/mobile-nav/link.svelte';
	import Button from '$lib/mobile-nav/button.svelte';

	
	let menuOpen = false;
	let inputValue = "";
	$:console.log(inputValue)
	
	const menuItems = ["About", "Base", "Blog", "Contact", "Custom", "Support", "Tools", "Boats", "Cars", "Bikes", "Sheds", "Billygoats", "Zebras", "Tennis Shoes", "New Zealand"];
	let filteredItems = [];
	
	const handleInput = () => {
		return filteredItems = menuItems.filter(item => item.toLowerCase().match(inputValue.toLowerCase()));	
	}



   let is_visible=true
   function toggle(){
    if(is_visible==false){
      is_visible=true
    }
    else{
      is_visible=false
    }
   }
</script>

<header>
	<nav _ngcontent-qgw-c49="" class="flex w-full z-10 text-gray-500 flex-wrap top-0 p-4 pt-6 -ml-4 ng-tns-c49-0 absolute snipcss-ED5Gw">
		<div _ngcontent-qgw-c49="" class="flex justify-between w-full lg:hidden ng-tns-c49-0">
		  <pivo-logo _ngcontent-qgw-c49="" class="ng-tns-c49-0">
			<div class="inline-block">
        <div class="mob-view-logo">
			  <a routerlink="/" href="#/" class="snip-a">
          <!-- <h1>FincoTel</h1> -->
				<pivo-image alt="Pivo logo" class="!h-8">
				  <picture>
					<source media="(min-width: 1024px)" srcset={fincotel}>
					<source media="(max-width: 1023px)" srcset={fincotel}>
					<img class="w-auto h-auto lg:h-full !h-8 snip-img" alt="Pivo logo" src={fincotel}>
				  </picture>
				</pivo-image>
			  </a>
      </div>
			</div>
		  </pivo-logo>
      
		  <button on:click={() => menuOpen = !menuOpen} {menuOpen} _ngcontent-qgw-c49="" class="flex h-6 flex-col justify-between items-end ng-tns-c49-0 snip-button" >
			<span _ngcontent-qgw-c49="" class="inline-block h-[3px] w-8 rounded-full ng-tns-c49-0 bg-white ng-star-inserted">
			</span>
			<span _ngcontent-qgw-c49="" class="inline-block h-[3px] w-6 rounded-full ng-tns-c49-0 bg-white ng-star-inserted">
			</span>
			<span _ngcontent-qgw-c49="" class="inline-block h-[3px] w-8 rounded-full ng-tns-c49-0 bg-white ng-star-inserted">
			</span>
      <div id="myDropdown" class:show={menuOpen} class="dropdown-content"style="margin-left: 0.5312rem;margin-top: -1.47rem;margin-right: -1.4688rem;">		
        
        <!-- MENU -->
        <!-- <mobnav/> -->
          <!-- {#each menuItems as item}
            <Link link={item} />
          {/each} -->
          <div _ngcontent-yld-c49="" class="flex justify-between w-full lg:hidden ng-tns-c49-0 snip-div">
            <pivo-logo _ngcontent-yld-c49="" class="ng-tns-c49-0">
              <div class="inline-block snip-div">
                <a routerlink="/" href="#/" class="snip-a">
                  <pivo-image alt="Pivo logo" class="!h-8">
                    <picture>
                      <source media="(min-width: 1024px)" srcset={fincotel}>
                      <source media="(max-width: 1023px)" srcset={fincotel}>
                      <img class="w-auto h-auto lg:h-full !h-8 snipcss0-0-0-1 tether-target-attached-top tether-element-attached-top tether-element-attached-center tether-target-attached-center snip-img" alt="Pivo logo" src={fincotel} style="margin: .5rem;">
                    </picture>
                  </pivo-image>
                </a>
              </div>
            </pivo-logo>
            <button _ngcontent-yld-c49="" class="flex h-6 flex-col justify-between items-end ng-tns-c49-0 snip-button">
              <i-feather _ngcontent-yld-c49="" name="x" class="text-gray-500 ng-tns-c49-0 ng-star-inserted" style="height: 42px; width: 42px;" _nghost-yld-c9="">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-x snip-svg">
                  <line x1="18" y1="6" x2="6" y2="18">
                  </line>
                  <line x1="6" y1="6" x2="18" y2="18">
                  </line>
                </svg>
              </i-feather>
            </button>
          </div>
          <ul _ngcontent-yld-c49="" class="w-full mt-10 text-xl gap-6 flex flex-wrap max-h-full overflow-y-scroll lg:hidden ng-tns-c49-0 ng-star-inserted snip-ul">
            <li _ngcontent-yld-c49="" class="w-full flex flex-wrap justify-between items-center ng-tns-c49-0 ng-star-inserted">
              <span _ngcontent-yld-c49="" class="ng-tns-c49-0 snip-span">
                <a _ngcontent-yld-c49="" href="#" class="ng-tns-c49-0 snip-a">
                  Products
                </a>
              </span>
              <span _ngcontent-yld-c49="" class="ng-tns-c49-0 snip-span">
                <i-feather _ngcontent-yld-c49="" style="width: 28px; height: 28px;" class="ng-tns-c49-0" _nghost-yld-c9="">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-chevron-right snip-svg">
                    <polyline points="9 18 15 12 9 6">
                    </polyline>
                  </svg>
                </i-feather>
              </span>
            </li>
            <li _ngcontent-yld-c49="" class="w-full ng-tns-c49-0">
              <a _ngcontent-yld-c49="" routerlink="about-us" class="ng-tns-c49-0 snip-a" href="#/about-us">
                About Us
              </a>
            </li>
            <li _ngcontent-yld-c49="" class="w-full ng-tns-c49-0 ng-star-inserted">
              <a _ngcontent-yld-c49="" routerlink="faq" class="ng-tns-c49-0 snip-a" href="#/faq">
                FAQs
              </a>
            </li>
            <li _ngcontent-yld-c49="" class="w-full mb-20 ng-tns-c49-0">
              <a _ngcontent-yld-c49="" routerlink="contact-us" class="ng-tns-c49-0 snip-a" href="#/contact-us">
                Contact Us
              </a>
            </li>
            <li _ngcontent-yld-c49="" class="ng-tns-c49-0">
              <a _ngcontent-yld-c49="" href="#" target="_blank" class="ng-tns-c49-0 snip-a">
                Blog
              </a>
            </li>
          </ul>
          <!---->
          <div _ngcontent-yld-c49="" class="lg:flex justify-between w-full hidden items-center px-14 xl:px-24 sm:px-16 justify-center ng-tns-c49-0 snip-div">
            <div _ngcontent-yld-c49="" class="w-[25%] ng-tns-c49-0 snip-div">
              <pivo-logo _ngcontent-yld-c49="" class="ng-tns-c49-0">
                <div class="inline-block snip-div">
                  <a routerlink="/" href="#/" class="snip-a">
                    <pivo-image alt="Pivo logo" class="!h-8">
                      <picture>
                        <source media="(min-width: 1024px)" srcset="https://pivo.africa/assets/images/pivo-dark.png">
                        <source media="(max-width: 1023px)" srcset="https://pivo.africa/assets/images/pivo-dark.png">
                        <img class="w-auto h-auto lg:h-full !h-8 snip-img" alt="Pivo logo" src="https://pivo.africa/assets/images/pivo-dark.png">
                      </picture>
                    </pivo-image>
                  </a>
                </div>
              </pivo-logo>
            </div>
            <ul _ngcontent-yld-c49="" class="flex gap-[50px] text-sm ng-tns-c49-0 text-white snip-ul">
              <li _ngcontent-yld-c49="" class="flex gap-[5px] product-link ng-tns-c49-0 ng-star-inserted">
                <span _ngcontent-yld-c49="" class="inline-block w-full cursor-pointer ng-tns-c49-0 snip-span">
                  Products
                </span>
                <span _ngcontent-yld-c49="" class="icon ng-tns-c49-0 snip-span">
                  <i-feather _ngcontent-yld-c49="" name="chevron-down" style="width: 12px; height: 12px;" class="ng-tns-c49-0" _nghost-yld-c9="">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-chevron-down snip-svg">
                      <polyline points="6 9 12 15 18 9">
                      </polyline>
                    </svg>
                  </i-feather>
                </span>
              </li>
              <li _ngcontent-yld-c49="" class="ng-tns-c49-0">
                <a _ngcontent-yld-c49="" routerlinkactive="text-primary-blue" routerlink="about-us" class="ng-tns-c49-0 snip-a" href="#/about-us">
                  About Us
                </a>
              </li>
              <li _ngcontent-yld-c49="" class="ng-tns-c49-0 ng-star-inserted">
                <a _ngcontent-yld-c49="" routerlinkactive="text-primary-blue" routerlink="faq" class="ng-tns-c49-0 snip-a" href="#/faq">
                  FAQs
                </a>
              </li>
              <li _ngcontent-yld-c49="" class="ng-tns-c49-0">
                <a _ngcontent-yld-c49="" routerlinkactive="font-semibold" routerlink="contact-us" class="ng-tns-c49-0 snip-a" href="#/contact-us">
                  Contact Us
                </a>
              </li>
              <li _ngcontent-yld-c49="" class="ng-tns-c49-0">
                <a _ngcontent-yld-c49="" href="http://blog.pivo.africa/" target="_blank" class="ng-tns-c49-0 snip-a">
                  Blog
                </a>
              </li>
            </ul>
            <div _ngcontent-yld-c49="" class="flex justify-end gap-4 xl:gap-6 items-center w-[25%] ng-tns-c49-0 ng-star-inserted snip-div">
              <span _ngcontent-yld-c49="" class="ng-tns-c49-0 text-white snip-span">
                <a _ngcontent-yld-c49="" target="_blank" class="ng-tns-c49-0 snip-a" href="https://app.pivo.africa/#/auth/login">
                  Sign in
                </a>
              </span>
              <button _ngcontent-yld-c49="" class="flex gap-1 justify-center text-[.7em] xl:text-sm items-center p-2 xl:px-[15px] xl:py-4 py-4 hover:shadow rounded-lg items-middle bg-primary-blue text-white ng-tns-c49-0 snip-button">
                <a _ngcontent-yld-c49="" target="_blank" class="ng-tns-c49-0 snip-a" href="https://app.pivo.africa/#/auth/signup">
                  Create an account
                </a>
                <i-feather _ngcontent-yld-c49="" name="arrow-right" class="animated-arrow ng-tns-c49-0" style="height: 14px; width: 14px;" _nghost-yld-c9="">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-arrow-right snip-svg">
                    <line x1="5" y1="12" x2="19" y2="12">
                    </line>
                    <polyline points="12 5 19 12 12 19">
                    </polyline>
                  </svg>
                </i-feather>
              </button>
            </div>
          </div>



      </div>	
		  </button>
      <!-- <Button on:click={() => menuOpen = !menuOpen} {menuOpen} /> -->
	
        <!-- <div id="myDropdown" class:show={menuOpen} class="dropdown-content">		 -->
        
          <!-- MENU -->
          <!-- <mobnav/> -->
            <!-- {#each menuItems as item}
              <Link link={item} />
            {/each}
          	
        </div>	 -->

		</div>
		<!---->
		<div _ngcontent-qgw-c49="" class="lg:flex justify-between w-full hidden items-center px-14 xl:px-24 sm:px-16 justify-center ng-tns-c49-0">
		  <div _ngcontent-qgw-c49="" class="w-[25%] ng-tns-c49-0">
			<pivo-logo _ngcontent-qgw-c49="" class="ng-tns-c49-0">
			  <div class="inline-block">
				<a routerlink="/" href="#/" class="snip-a">
          <!-- <h1>FincoTel</h1> -->
				  <pivo-image alt="Pivo logo" class="!h-8">
             
					<picture>
					  <source media="(min-width: 1024px)" srcset={fincotel}>
					  <source media="(max-width: 1023px)" srcset={fincotel}>
					  <img class="w-auto h-auto lg:h-full !h-8 snip-img" alt="Pivo logo" src={fincotel}>
					</picture>
				  </pivo-image>
				</a>
			  </div>
			</pivo-logo>
		  </div>
		  <ul _ngcontent-qgw-c49="" class="flex gap-[50px] text-sm ng-tns-c49-0 text-white snip-ul">
			<li _ngcontent-qgw-c49="" class="flex gap-[5px] product-link ng-tns-c49-0 ng-star-inserted">
			  <span _ngcontent-qgw-c49="" class="inline-block w-full cursor-pointer ng-tns-c49-0">
				Products
			  </span>
			  
			</li>
			<li _ngcontent-qgw-c49="" class="ng-tns-c49-0">
			  <a _ngcontent-qgw-c49="" routerlinkactive="text-primary-blue" routerlink="about-us" class="ng-tns-c49-0 snip-a" href="#/about-us">
				About Us
			  </a>
			</li>
			<li _ngcontent-qgw-c49="" class="ng-tns-c49-0 ng-star-inserted">
			  <a _ngcontent-qgw-c49="" routerlinkactive="text-primary-blue" routerlink="faq" class="ng-tns-c49-0 snip-a" href="#/faq">
				FAQs
			  </a>
			</li>
			<li _ngcontent-qgw-c49="" class="ng-tns-c49-0">
			  <a _ngcontent-qgw-c49="" routerlinkactive="font-semibold" routerlink="contact-us" class="ng-tns-c49-0 snip-a" href="#/contact-us">
				Contact Us
			  </a>
			</li>
			<li _ngcontent-qgw-c49="" class="ng-tns-c49-0">
			  <a _ngcontent-qgw-c49="" routerlinkactive="font-semibold" routerlink="blog" class="ng-tns-c49-0 snip-a" href="#/blog">
				Blog
			  </a>
			</li>
		  </ul>
		  <div _ngcontent-qgw-c49="" class="flex justify-end gap-4 xl:gap-6 items-center w-[25%] ng-tns-c49-0 ng-star-inserted" style="margin-left: 1rem;">
			<span _ngcontent-qgw-c49="" class="ng-tns-c49-0 text-white">
			  <a _ngcontent-qgw-c49="" target="_blank" routerlinkactive="font-semibold" routerlink="sign-in" class="ng-tns-c49-0 snip-a" href="#/sign-in" style="font-size: 1.2rem;">
				Sign in
			  </a>
			</span>
			<button _ngcontent-qgw-c49="" class="flex gap-1 justify-center text-[.7em] xl:text-sm items-center p-2 xl:px-[15px] xl:py-4 py-4 hover:shadow rounded-lg items-middle bg-primary-blue text-white ng-tns-c49-0 snip-button">
			  <a _ngcontent-qgw-c49="" target="_blank"  routerlinkactive="font-semibold" routerlink="Create-an-account" class="ng-tns-c49-0 snip-a" href="#/Create-an-account" style="font-size: 1.1rem;">
				Create an account
			  </a>
			  <i-feather _ngcontent-qgw-c49="" name="arrow-right" class="animated-arrow ng-tns-c49-0" style="height: 14px; width: 14px;" _nghost-qgw-c9="">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-arrow-right snip-svg">
				  <line x1="5" y1="12" x2="19" y2="12">
				  </line>
				  <polyline points="12 5 19 12 12 19">
				  </polyline>
				</svg>
			  </i-feather>
			</button>
		  </div>
		</div>
		<!---->
		<!---->
	  </nav>
	  
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}
  .mob-view-logo{
    padding-bottom: 20px;
  }
	@font-face { 
  font-family:Inter;
  src:url(https://pivo.africa/Inter-Regular.f40d63d7760e63dd.ttf) format("TrueType");
} 
@import url("https://fonts.googleapis.com/css?family=Poppins|Roboto"); 
* { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
} 

@media all{ 
  * { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
  } 
}     

@media all{ 
  .px-4 { 
    padding-left: 1rem; 
    padding-right: 1rem;
  } 
}     

@media all{ 
  .font-primary { 
    font-family: Inter;
  } 
}     

body { 
    margin:    0;
    font-family:   inherit; 
    line-height:  inherit;
    overflow-x: hidden; 
    scroll-behavior: smooth;
} 

@media all{ 
  body { 
    margin:    0;
    font-family:   inherit; 
    line-height:  inherit;
    overflow-x: hidden; 
    scroll-behavior: smooth;
  } 
}     

html { 
    tab-size:    4;
    line-height:   1.5;
    -webkit-text-size-adjust:   100%;
    font-family:  ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,"Apple Color Emoji","Segoe UI Emoji",Segoe UI Symbol,"Noto Color Emoji"; 
    overflow-x: hidden; 
    scroll-behavior: smooth;
} 

@media all{ 
  html { 
    tab-size:    4;
    line-height:   1.5;
    -webkit-text-size-adjust:   100%;
    font-family:  ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,"Apple Color Emoji","Segoe UI Emoji",Segoe UI Symbol,"Noto Color Emoji"; 
    overflow-x: hidden; 
    scroll-behavior: smooth;
  } 
}     

@media all{ 
  .absolute { 
    position: absolute;
  } 
}     

@media all{ 
  .top-0 { 
    top: 0px;
  } 
}     

@media all{ 
  .z-10 { 
    z-index: 10;
  } 
}     

@media all{ 
  .-ml-4 { 
    margin-left: -1rem;
  } 
}     

@media all{ 
  .flex { 
    display: flex;
  } 
}     

@media all{ 
  .w-full { 
    width: 100%;
  } 
}     

@media all{ 
  .flex-wrap { 
    flex-wrap: wrap;
  } 
}     

@media all{ 
  .p-4 { 
    padding: 1rem;
  } 
}     

@media all{ 
  .pt-6 { 
    padding-top: 1.5rem;
  } 
}     

@media all{ 
  .text-gray-500 { 
    --tw-text-opacity: 1; 
    color: rgba(107,114,128,var(--tw-text-opacity));
  } 
}     

*,:before,:after { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
} 

@media all{ 
  *,:before,:after { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
  } 
}     

@media all{ 
  .justify-between { 
    justify-content: space-between;
  } 
}     

@media (min-width: 1024px){ 
  .lg\:hidden { 
    display: none;
  } 
}     

@media all{ 
  .hidden { 
    display: none;
  } 
}     

@media all{ 
  .items-center { 
    align-items: center;
  } 
}     

@media all{ 
  .justify-center { 
    justify-content: center;
  } 
}     

@media all{ 
  .px-14 { 
    padding-left: 3.5rem; 
    padding-right: 3.5rem;
  } 
}     

@media (min-width: 640px){ 
  .sm\:px-16 { 
    padding-left: 4rem; 
    padding-right: 4rem;
  } 
}     

@media (min-width: 1024px){ 
  .lg\:flex { 
    display: flex;
  } 
}     

@media all{ 
  button { 
    font-family:      inherit; 
    font-size:      100%; 
    line-height:  inherit; 
    margin:      0;
    text-transform:     none;
    -webkit-appearance:    button;
    background-color:   transparent; 
    background-image:   none;
    cursor:  pointer;
    padding: 0; 
    color: inherit;
  } 
}     

@media all{ 
  .h-6 { 
    height: 1.5rem;
  } 
}     

@media all{ 
  .flex-col { 
    flex-direction: column;
  } 
}     

@media all{ 
  .items-end { 
    align-items: flex-end;
  } 
}     

@media all{ 
  .w-\[25\%\] { 
    width: 25%;
  } 
}     

@media all{ 
  ul { 
    list-style: none; 
    margin: 0; 
    padding: 0;
  } 
}     

@media all{ 
  .gap-\[50px\] { 
    gap: 50px;
  } 
}     

@media all{ 
  .text-sm { 
    font-size: 1.1rem; 
    line-height: 1.25rem;
  } 
}     

@media all{ 
  .text-white { 
    --tw-text-opacity: 1; 
    color: rgba(254,254,254,var(--tw-text-opacity));
  } 
}     

@media all{ 
  .justify-end { 
    justify-content: flex-end;
  } 
}     

@media all{ 
  .gap-4 { 
    gap: 1rem;
  } 
}     

@media all{ 
  .inline-block { 
    display: inline-block;
  } 
}     

@media all{ 
  .h-\[3px\] { 
    height: 3px;
  } 
}     

@media all{ 
  .w-8 { 
    width: 2rem;
  } 
}     

@media all{ 
  .rounded-full { 
    border-radius: 9999px;
  } 
}     

@media all{ 
  .bg-white { 
    --tw-bg-opacity: 1; 
    background-color: rgba(254,254,254,var(--tw-bg-opacity));
  } 
}     

@media all{ 
  .w-6 { 
    width: 1.5rem;
  } 
}     

@media all{ 
  .gap-\[5px\] { 
    gap: 5px;
  } 
}     

.product-link[_ngcontent-qgw-c49] { 
    position: relative;
} 

@media all{ 
  .gap-1 { 
    gap: .25rem;
  } 
}     

@media all{ 
  .rounded-lg { 
    border-radius: .5rem;
  } 
}     

@media all{ 
  .bg-primary-blue { 
    --tw-bg-opacity: 1; 
    background-color: rgba(1,101,254,var(--tw-bg-opacity));
  } 
}     

@media all{ 
  .p-2 { 
    padding: .5rem;
  } 
}     

@media all{ 
  .py-4 { 
    padding-top: 1rem; 
    padding-bottom: 1rem;
  } 
}     

@media all{ 
  .text-\[\.7em\] { 
    font-size: .7em;
  } 
}     

@media all{ 
  .hover\:shadow:hover { 
    --tw-shadow: 0 1px 3px 0 rgba(0, 0, 0, .1), 0 1px 2px 0 rgba(0, 0, 0, .06); 
    box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),var(--tw-ring-shadow, 0 0 #0000),var(--tw-shadow);
  } 
}     

@media all{ 
  a { 
    color: inherit; 
    text-decoration: inherit;
  } 
}     

@media all{ 
  .cursor-pointer { 
    cursor: pointer;
  } 
}     

.product-link[_ngcontent-qgw-c49]:hover > .icon[_ngcontent-qgw-c49]  { 
    position: relative; 
    --tw-translate-y: .25rem; 
    transform: var(--tw-transform); 
    transition-property: all; 
    transition-timing-function: cubic-bezier(.4,0,.2,1); 
    transition-duration: .5s;
} 

[_nghost-qgw-c9] { 
    display: inline-block; 
    fill: none; 
    height: 24px; 
    stroke: currentColor; 
    stroke-linecap: round; 
    stroke-linejoin: round; 
    stroke-width: 2px; 
    width: 24px;
} 
.inline-block h1{
color:white;
font-size:30px

}
@media all{ 
  .\!h-8 { 
    height: 2rem!important;
  } 
}     

@media all{ 
  svg { 
    display: block; 
    vertical-align: middle;
  } 
}     

@media all{ 
  img { 
    border-style:   solid;
    display:  block; 
    vertical-align:  middle;
    max-width: 100%; 
    height: auto;
  } 
}     

@media all{ 
  .h-auto { 
    height: auto;
  } 
}     

@media all{ 
  .w-auto { 
    width: auto;
  } 
}     

@media (min-width: 1024px){ 
  .lg\:h-full { 
    height: 100%;
  } 
}     

/* menu mob stuff */



.dropdown {
  position: relative;
  display: inline-block;
}
	
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f6f6f6;
  min-width: 230px;
  border: 1px solid #ddd;
  z-index: 1;
}

/* Show the dropdown menu */	
.show {display:block;}
@import url("https://fonts.googleapis.com/css?family=Poppins|Roboto"); 
@import url("https://fonts.googleapis.com/css?family=Poppins|Roboto"); 
@font-face { 
  font-family:Inter;
  src:url(https://pivo.africa/Inter-Regular.f40d63d7760e63dd.ttf) format("TrueType");
} 
* { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
} 

@media all{ 
  * { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
  } 
}     

@media all{ 
  .px-4 { 
    padding-left: 1rem; 
    padding-right: 1rem;
  } 
}     

@media all{ 
  .font-primary { 
    font-family: Inter;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:text-\[16px\] { 
    font-size: 16px;
  } 
}     

body { 
    margin:    0;
    font-family:   inherit; 
    line-height:  inherit;
    overflow-x: hidden; 
    scroll-behavior: smooth;
} 

@media all{ 
  body { 
    margin:    0;
    font-family:   inherit; 
    line-height:  inherit;
    overflow-x: hidden; 
    scroll-behavior: smooth;
  } 
}     

body { 
    user-select: text !important;
} 

html { 
    tab-size:    4;
    line-height:   1.5;
    -webkit-text-size-adjust:   100%;
    font-family:  ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,"Apple Color Emoji","Segoe UI Emoji",Segoe UI Symbol,"Noto Color Emoji"; 
    overflow-x: hidden; 
    scroll-behavior: smooth;
} 

@media all{ 
  html { 
    tab-size:    4;
    line-height:   1.5;
    -webkit-text-size-adjust:   100%;
    font-family:  ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,"Apple Color Emoji","Segoe UI Emoji",Segoe UI Symbol,"Noto Color Emoji"; 
    overflow-x: hidden; 
    scroll-behavior: smooth;
  } 
}     

@media all{ 
  .fixed { 
    position: fixed;
  } 
}     

@media all{ 
  .top-0 { 
    top: 0px;
  } 
}     

@media all{ 
  .z-10 { 
    z-index: 10;
  } 
}     

@media all{ 
  .-ml-4 { 
    margin-left: -1rem;
  } 
}     

@media all{ 
  .flex { 
    display: flex;
  } 
}     

@media all{ 
  .h-screen { 
    height: 100vh;
  } 
}     

@media all{ 
  .w-full { 
    width: 100%;
  } 
}     

@media all{ 
  .flex-wrap { 
    flex-wrap: wrap;
  } 
}     

@media all{ 
  .content-start { 
    align-content: flex-start;
  } 
}     

@media all{ 
  .bg-white { 
    --tw-bg-opacity: 1; 
    background-color: rgba(254,254,254,var(--tw-bg-opacity));
  } 
}     

@media all{ 
  .p-4 { 
    padding: 1rem;
  } 
}     

@media all{ 
  .pt-6 { 
    padding-top: 1.5rem;
  } 
}     

@media all{ 
  .text-gray-500 { 
    --tw-text-opacity: 1; 
    color: rgba(107,114,128,var(--tw-text-opacity));
  } 
}     

*,:before,:after { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
} 

@media all{ 
  *,:before,:after { 
    box-sizing:   border-box; 
    border-width:  0; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
    --tw-transform: translateX(var(--tw-translate-x)) translateY(var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y)); 
    --tw-border-opacity: 1; 
    --tw-shadow: 0 0 #0000; 
    --tw-blur: var(--tw-empty, ); 
    --tw-brightness: var(--tw-empty, ); 
    --tw-contrast: var(--tw-empty, ); 
    --tw-grayscale: var(--tw-empty, ); 
    --tw-hue-rotate: var(--tw-empty, ); 
    --tw-invert: var(--tw-empty, ); 
    --tw-saturate: var(--tw-empty, ); 
    --tw-sepia: var(--tw-empty, ); 
    --tw-drop-shadow: var(--tw-empty, ); 
  } 
}     

:selection { 
    background-color: #338FFF !important; 
    color: #fff !important;
} 

div { 
    user-select: text !important;
} 

@media all{ 
  .justify-between { 
    justify-content: space-between;
  } 
}     

@media (min-width: 1024px){ 
  .lg\:hidden { 
    display: none;
  } 
}     

@media all{ 
  ul { 
    list-style: none; 
    margin: 0; 
    padding: 0;
  } 
}     

@media all{ 
  .mt-10 { 
    margin-top: 2.5rem;
  } 
}     

@media all{ 
  .max-h-full { 
    max-height: 100%;
  } 
}     

@media all{ 
  .gap-6 { 
    gap: 1.5rem;
  } 
}     

@media all{ 
  .overflow-y-scroll { 
    overflow-y: scroll;
  } 
}     

@media all{ 
  .text-xl { 
    font-size: 1.25rem; 
    line-height: 1.75rem;
  } 
}     

@media all{ 
  .hidden { 
    display: none;
  } 
}     

@media all{ 
  .items-center { 
    align-items: center;
  } 
}     

@media all{ 
  .justify-center { 
    justify-content: center;
  } 
}     

@media all{ 
  .px-14 { 
    padding-left: 3.5rem; 
    padding-right: 3.5rem;
  } 
}     

@media (min-width: 640px){ 
  .sm\:px-16 { 
    padding-left: 4rem; 
    padding-right: 4rem;
  } 
}     

@media (min-width: 1024px){ 
  .lg\:flex { 
    display: flex;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:px-24 { 
    padding-left: 6rem; 
    padding-right: 6rem;
  } 
}     

@media all{ 
  button { 
    font-family:      inherit; 
    font-size:      100%; 
    line-height:  inherit; 
    margin:      0;
    text-transform:     none;
    -webkit-appearance:    button;
    background-color:   transparent; 
    background-image:   none;
    cursor:  pointer;
    padding: 0; 
    color: inherit;
  } 
}     

@media all{ 
  .h-6 { 
    height: 1.5rem;
  } 
}     

@media all{ 
  .flex-col { 
    flex-direction: column;
  } 
}     

@media all{ 
  .items-end { 
    align-items: flex-end;
  } 
}     

@media all{ 
  .mb-20 { 
    margin-bottom: 5rem;
  } 
}     

@media all{ 
  .w-\[25\%\] { 
    width: 25%;
  } 
}     

@media all{ 
  .gap-\[50px\] { 
    gap: 50px;
  } 
}     

@media all{ 
  .text-sm { 
    font-size: .875rem; 
    line-height: 1.25rem;
  } 
}     

@media all{ 
  .text-white { 
    --tw-text-opacity: 1; 
    color: rgba(254,254,254,var(--tw-text-opacity));
  } 
}     

@media all{ 
  .justify-end { 
    justify-content: flex-end;
  } 
}     

@media all{ 
  .gap-4 { 
    gap: 1rem;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:gap-6 { 
    gap: 1.5rem;
  } 
}     

@media all{ 
  .inline-block { 
    display: inline-block;
  } 
}     

[_nghost-yld-c9] { 
    display: inline-block; 
    fill: none; 
    height: 24px; 
    stroke: currentColor; 
    stroke-linecap: round; 
    stroke-linejoin: round; 
    stroke-width: 2px; 
    width: 24px;
} 

span { 
    user-select: text !important;
} 

@media all{ 
  a { 
    color: inherit; 
    text-decoration: inherit;
  } 
}     

a { 
    user-select: text !important;
} 

@media all{ 
  .gap-\[5px\] { 
    gap: 5px;
  } 
}     

.product-link[_ngcontent-yld-c49] { 
    position: relative;
} 

@media all{ 
  .gap-1 { 
    gap: .25rem;
  } 
}     

@media all{ 
  .rounded-lg { 
    border-radius: .5rem;
  } 
}     

@media all{ 
  .bg-primary-blue { 
    --tw-bg-opacity: 1; 
    background-color: rgba(1,101,254,var(--tw-bg-opacity));
  } 
}     

@media all{ 
  .p-2 { 
    padding: .5rem;
  } 
}     

@media all{ 
  .py-4 { 
    padding-top: 1rem; 
    padding-bottom: 1rem;
  } 
}     

@media all{ 
  .text-\[\.7em\] { 
    font-size: .7em;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:px-\[15px\] { 
    padding-left: 15px; 
    padding-right: 15px;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:py-4 { 
    padding-top: 1rem; 
    padding-bottom: 1rem;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:text-sm { 
    font-size: .875rem; 
    line-height: 1.25rem;
  } 
}     

@media all{ 
  .hover\:shadow:hover { 
    --tw-shadow: 0 1px 3px 0 rgba(0, 0, 0, .1), 0 1px 2px 0 rgba(0, 0, 0, .06); 
    box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),var(--tw-ring-shadow, 0 0 #0000),var(--tw-shadow);
  } 
}     

@media all{ 
  svg { 
    display: block; 
    vertical-align: middle;
  } 
}     

@media all{ 
  .cursor-pointer { 
    cursor: pointer;
  } 
}     

.product-link[_ngcontent-yld-c49]:hover > .icon[_ngcontent-yld-c49]  { 
    position: relative; 
    --tw-translate-y: .25rem; 
    transform: var(--tw-transform); 
    transition-property: all; 
    transition-timing-function: cubic-bezier(.4,0,.2,1); 
    transition-duration: .5s;
} 

@media all{ 
  .\!h-8 { 
    height: 2rem!important;
  } 
}     

@media all{ 
  img { 
    border-style:   solid;
    display:  block; 
    vertical-align:  middle;
    max-width: 100%; 
    height: auto;
  } 
}     

@media all{ 
  .h-auto { 
    height: auto;
  } 
}     

@media all{ 
  .w-auto { 
    width: auto;
  } 
}     

@media (min-width: 1024px){ 
  .lg\:h-full { 
    height: 100%;
  } 
}     

</style>
