<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
	import Footer from '$lib/footer/Footer.svelte'
	import MPage from "./+page.svelte"
	import Legal from "./legal.svelte";

	import fincotel from "$lib/assets/fincotel.png";

	
let menuOpen = false;
function scrollIntoView({ target }) {
	const el = document.querySelector(target.getAttribute('href'));
	if (!el) return;
el.scrollIntoView({
  behavior: 'smooth'
});
}






	 let mainer=true;
 function toggle1 (){
   console.log(mainer)
 if (mainer){
   mainer=false
 }
}
function toggle2 (){
   console.log(mainer)
 if (!mainer){
   mainer=true
 }
}

</script>



<header>
	<nav _ngcontent-qgw-c49="" class="flex w-full z-10 text-gray-500 flex-wrap top-0 p-4 pt-6 -ml-4 ng-tns-c49-0 absolute snipcss-ED5Gw">
		<div _ngcontent-qgw-c49="" class="flex justify-between w-full lg:hidden ng-tns-c49-0">
		  <pivo-logo _ngcontent-qgw-c49="" class="ng-tns-c49-0">
			<div class="inline-block">
        <div class="mob-view-logo">
			  <a on:click={toggle2} class="snip-a">
				<pivo-image alt="FincoTel Logo" class="!h-8">
				  <picture>
					<source media="(min-width: 1024px)" srcset={fincotel}>
					<source media="(max-width: 1023px)" srcset={fincotel}>
					<img class="w-auto h-auto lg:h-full !h-8 snip-img" alt="FincoTel Logo" src={fincotel}>
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
      <div id="myDropdown" class:show={menuOpen} class="dropdown-content" style="
      /* margin-left: 109.5312rem; */
      /* margin-top: -1.47rem; */
      /* margin-right: -1.4688rem; */
      /* opacity: 0.8; */
      /* background-color:#ccc; */
      position:
      fixed;
      width:100%;
      height:100%;
      top:0px;
      left:0px;
      z-index:1000;
      /* flex: auto; */
      /* justify-content: center; */
      ">		
        
        
          <div _ngcontent-yld-c49="" class="flex justify-between w-full lg:hidden ng-tns-c49-0 snip-div">
            <pivo-logo _ngcontent-yld-c49="" class="ng-tns-c49-0">
              <div class="inline-block snip-div">
                <a on:click={toggle2} class="snip-a">
                  <pivo-image alt="FincoTel Logo" class="!h-8">
                    <picture>
                      <source media="(min-width: 1024px)" srcset={fincotel}>
                      <source media="(max-width: 1023px)" srcset={fincotel}>
                      <img class="w-auto h-auto lg:h-full !h-8 snipcss0-0-0-1 tether-target-attached-top tether-element-attached-top tether-element-attached-center tether-target-attached-center snip-img" alt="FincoTel Logo" src={fincotel} style="margin: .5rem;">
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
          <ul _ngcontent-yld-c49="" class="w-full mt-10 text-xl gap-6 flex flex-wrap max-h-full overflow-y-scroll lg:hidden ng-tns-c49-0 ng-star-inserted snip-ul" style="
          margin-left: 1rem;
          margin-right: 1rem;
      ">
            <li style="
            display: inline-block;padding:1rem;"
         _ngcontent-yld-c49="" class="w-full flex flex-wrap justify-between items-center ng-tns-c49-0 ng-star-inserted">
              <span _ngcontent-yld-c49="" class="ng-tns-c49-0 snip-span">
                <a _ngcontent-yld-c49="" href="#" class="ng-tns-c49-0 snip-a">
                  Products
                </a>
              </span>
             
            </li>
            <li _ngcontent-yld-c49="" class="w-full ng-tns-c49-0"style="
            display: inline-block;padding:1rem;">
              <a _ngcontent-yld-c49="" routerlink="about-us" class="ng-tns-c49-0 snip-a" href="#/about-us">
                About Us
              </a>
            </li>
            <li _ngcontent-yld-c49="" class="w-full ng-tns-c49-0 ng-star-inserted" style="
            display: inline-block;padding:1rem;">
              <a on:click|preventDefault={scrollIntoView} _ngcontent-yld-c49="" routerlink="faq" class="ng-tns-c49-0 snip-a" href="#faq">
                FAQs
              </a>
            </li>
            <li _ngcontent-yld-c49="" class="w-full mb-20 ng-tns-c49-0"style="
            display: inline-block;padding:1rem;">
              <a _ngcontent-yld-c49="" routerlink="contact-us" class="ng-tns-c49-0 snip-a" href="#/contact-us">
                Contact Us
              </a>
            </li>
            <li _ngcontent-yld-c49="" class="ng-tns-c49-0" style="
            width: 100%;
         inline-block;padding:1rem;">
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
                  <a on:click={toggle2} class="snip-a">
                    <pivo-image alt="FincoTel Logo" class="!h-8">
                      <picture>
                        <source media="(min-width: 1024px)" srcset={fincotel}>
                        <source media="(max-width: 1023px)" srcset={fincotel}>
                        <img class="w-auto h-auto lg:h-full !h-8 snip-img" alt="FincoTel Logo" src={fincotel}>
                      </picture>
                    </pivo-image>
                  </a>
                </div>
              </pivo-logo>
            </div>
            <ul _ngcontent-yld-c49="" class="flex gap-[50px] text-sm ng-tns-c49-0 text-white snip-ul"style="
			font-size: 1.1rem;
		">
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
                <a  on:click|preventDefault={scrollIntoView} _ngcontent-yld-c49="" routerlinkactive="text-primary-blue" routerlink="faq" class="ng-tns-c49-0 snip-a" href="#faq">
                  FAQs
                </a>
              </li>
              <li _ngcontent-yld-c49="" class="ng-tns-c49-0">
                <a _ngcontent-yld-c49="" routerlinkactive="font-semibold" routerlink="contact-us" class="ng-tns-c49-0 snip-a" href="#/contact-us">
                  Contact Us
                </a>
              </li>
              <li _ngcontent-yld-c49="" class="ng-tns-c49-0">
                <a _ngcontent-yld-c49="" href="#" target="_blank" class="ng-tns-c49-0 snip-a">
                  Blog
                </a>
              </li>
            </ul>
            <div _ngcontent-yld-c49="" class="flex justify-end gap-4 xl:gap-6 items-center w-[25%] ng-tns-c49-0 ng-star-inserted snip-div">
              <span _ngcontent-yld-c49="" class="ng-tns-c49-0 text-white snip-span">
                <a _ngcontent-yld-c49="" target="_blank" class="ng-tns-c49-0 snip-a" href="#">
                  Sign in
                </a>
              </span>
              <button _ngcontent-yld-c49="" class="flex gap-1 justify-center text-[.7em] xl:text-sm items-center p-2 xl:px-[15px] xl:py-4 py-4 hover:shadow rounded-lg items-middle bg-primary-blue text-white ng-tns-c49-0 snip-button">
                <a _ngcontent-yld-c49="" target="_blank" class="ng-tns-c49-0 snip-a" href="#">
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
     
		</div>
		<!---->
		<div _ngcontent-qgw-c49="" class="lg:flex justify-between w-full hidden items-center px-14 xl:px-24 sm:px-16 justify-center ng-tns-c49-0">
		  <div _ngcontent-qgw-c49="" class="w-[25%] ng-tns-c49-0">
			<pivo-logo _ngcontent-qgw-c49="" class="ng-tns-c49-0">
			  <div class="inline-block">
				<a on:click={toggle2} class="snip-a">
          <!-- <h1>FincoTel</h1> -->
				  <pivo-image alt="FincoTel Logo" class="!h-8">
             
					<picture>
					  <source media="(min-width: 1024px)" srcset={fincotel}>
					  <source media="(max-width: 1023px)" srcset={fincotel}>
					  <img class="w-auto h-auto lg:h-full !h-8 snip-img" alt="FincoTel Logo" src={fincotel}>
					</picture>
				  </pivo-image>
				</a>
			  </div>
			</pivo-logo>
		  </div>
		  <ul _ngcontent-qgw-c49="" class="flex gap-[50px] text-sm ng-tns-c49-0 text-white snip-ul"style="
		  font-size: 1.1rem;
	  ">
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
			  <a  on:click|preventDefault={scrollIntoView} _ngcontent-qgw-c49="" routerlinkactive="text-primary-blue" routerlink="faq" class="ng-tns-c49-0 snip-a" href="#faq">
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

<main>
{#if mainer}
	<MPage />
	{:else}
	<!-- else content here -->
   <Legal />
{/if}
</main>


<footer _ngcontent-chr-c50="" class="bg-dark-blue pt-24 px-4 sm:px-16 xl:pb-14 xl:flex xl:flex-wrap xl:justify-between xl:px-24 snipcss0-0-0-1 snipcss-LdnHI" style="flex-flow: wrap;">
	<div _ngcontent-chr-c50="" class="flex flex-wrap xl:w-[29%] snipcss0-1-1-2 snip-div">
	  <h2 _ngcontent-chr-c50="" class="text-white font-semibold xl:text-xl snipcss0-2-2-3 snip-h2">
		Sign up to our newsletter 
	  </h2>
	  <form _ngcontent-chr-c50="" novalidate="" class="mt-8 mb-24 w-full flex flex-col ng-untouched ng-pristine ng-valid snipcss0-2-2-4">
		<label _ngcontent-chr-c50="" class="w-full sm:w-6/12 xl:w-8/12 snipcss0-3-4-5">
		  <span _ngcontent-chr-c50="" class="sr-only snipcss0-4-5-6 snip-span">
			Email
		  </span>
		  <input _ngcontent-chr-c50="" name="email" type="email" placeholder="Enter your email address" class="rounded-lg focus:outline-none focus:ring ring-light-blue p-6 py-4 placeholder-gray-100 bg-white/30 w-full ng-untouched ng-pristine ng-valid snipcss0-4-5-7">
		</label>
		<button _ngcontent-chr-c50="" class="mt-4 rounded-lg flex xl:text-lg max-w-[110px] xl:max-w-[120px] gap-2 items-center py-2 px-4 text-white bg-primary-blue snipcss0-3-4-8 snip-button">
		  <span _ngcontent-chr-c50="" class="snipcss0-4-8-9 snip-span">
			submit
		  </span>
		  <i-feather _ngcontent-chr-c50="" class="transform-all snipcss0-4-8-10" _nghost-chr-c9="">
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-arrow-right snipcss0-5-10-11 snip-svg">
			  <line x1="5" y1="12" x2="19" y2="12">
			  </line>
			  <polyline points="12 5 19 12 12 19">
			  </polyline>
			</svg>
		  </i-feather>
		</button>
	  </form>
	</div>
	<div _ngcontent-chr-c50="" class="text-[#FEFEFE] sm:gap-0 sm:justify-between xl:w-[65%] mb-24 xl:mb-16 flex flex-wrap gap-8 snipcss0-1-1-12 snip-div">
	  <nav _ngcontent-chr-c50="" class="w-5/12 sm:w-[28%] flex flex-col gap-6 snipcss0-2-12-13">
		<h2 _ngcontent-chr-c50="" class="font-bold snipcss0-3-13-14 snip-h2">
		  Company
		</h2>
		<ul _ngcontent-chr-c50="" class="flex flex-col gap-4 text-xs xl:text-base snipcss0-3-13-15 snip-ul">
		  <li _ngcontent-chr-c50="" class="snipcss0-4-15-16">
			<a _ngcontent-chr-c50="" routerlink="about-us" href="#/about-us" class="snipcss0-5-16-17 snip-a">
			  About
			</a>
		  </li>
		  <li _ngcontent-chr-c50="" class="snipcss0-4-15-18">
			<a _ngcontent-chr-c50="" routerlink="faq" href="#/faq" class="snipcss0-5-18-19 snip-a">
			  FAQs
			</a>
		  </li>
		  <li _ngcontent-chr-c50="" class="snipcss0-4-15-20">
			<button _ngcontent-chr-c50="" class="snipcss0-5-20-21 snip-button">
			  Privacy Policy
			</button>
		  </li>
		  <li _ngcontent-chr-c50="" class="snipcss0-4-15-22">
			<button _ngcontent-chr-c50="" class="snipcss0-5-22-23 snip-button">
			  Terms &amp; Conditions
			</button>
		  </li>
		  <li _ngcontent-chr-c50="" class="snipcss0-4-15-22">
			<button on:click|self={toggle1} class="snipcss0-5-16-17 snip-a">
			  Legal Policy
			</button>
		  </li>
		  
		</ul>
	  </nav>
	  <div _ngcontent-chr-c50="" class="w-5/12 sm:w-[28%] flex flex-col gap-6 snipcss0-2-12-24 snip-div">
		<h2 _ngcontent-chr-c50="" class="font-bold snipcss0-3-24-25 snip-h2">
		  Contact
		</h2>
		<div _ngcontent-chr-c50="" class="flex flex-col gap-4 text-xs xl:text-base snipcss0-3-24-26 snip-div">
		  <div _ngcontent-chr-c50="" class="snipcss0-4-26-27 snip-div">
			<a _ngcontent-chr-c50="" href="#/" class="snipcss0-5-27-28 snip-a">
			  hello@fincotel.online
			</a>
		  </div>
		  <!-- <div _ngcontent-chr-c50="" class="snipcss0-4-26-29 snip-div">
			<a _ngcontent-chr-c50="" href="tel://+2348061498208" class="snipcss0-5-29-30 snip-a">
			  (234) 806 149 8208
			</a>
		  </div> -->
		  <div _ngcontent-chr-c50="" class="flex gap-4 socials snipcss0-4-26-31 snip-div">
			<a _ngcontent-chr-c50="" target="_blank" href="https://www.linkedin.com/company/fincotel-online/" class="snipcss0-5-31-32 snip-a">
			  <i-feather _ngcontent-chr-c50="" name="linkedin" style="height: 14px; width: 14px; fill: #fefefe;" _nghost-chr-c9="" class="snipcss0-6-32-33">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-linkedin snipcss0-7-33-34 snip-svg">
				  <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z">
				  </path>
				  <rect x="2" y="9" width="4" height="12">
				  </rect>
				  <circle cx="4" cy="4" r="2">
				  </circle>
				</svg>
			  </i-feather>
			</a>
			<a _ngcontent-chr-c50="" target="_blank" href="#/" class="snipcss0-5-31-35 snip-a">
			  <i-feather _ngcontent-chr-c50="" name="twitter" style="height: 14px; width: 14px; fill: #fefefe;" _nghost-chr-c9="" class="snipcss0-6-35-36">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-twitter snipcss0-7-36-37 snip-svg">
				  <path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z">
				  </path>
				</svg>
			  </i-feather>
			</a>
			<a _ngcontent-chr-c50="" target="_blank" href="#/" class="snipcss0-5-31-38 snip-a">
			  <i-feather _ngcontent-chr-c50="" name="instagram" style="height: 14px; width: 14px; fill: #fefefe; stroke: #054da3;" _nghost-chr-c9="" class="snipcss0-6-38-39">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-instagram snipcss0-7-39-40 snip-svg">
				  <rect x="2" y="2" width="20" height="20" rx="5" ry="5">
				  </rect>
				  <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z">
				  </path>
				  <line x1="17.5" y1="6.5" x2="17.51" y2="6.5">
				  </line>
				</svg>
			  </i-feather>
			</a>
			<a _ngcontent-chr-c50="" target="_blank" href="#/" class="snipcss0-5-31-41 snip-a">
			  <i-feather _ngcontent-chr-c50="" name="facebook" style="height: 14px; width: 14px; fill: #fefefe;" _nghost-chr-c9="" class="snipcss0-6-41-42">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="feather feather-facebook snipcss0-7-42-43 snip-svg">
				  <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z">
				  </path>
				</svg>
			  </i-feather>
			</a>
		  </div>
		</div>
	  </div>
	  <div _ngcontent-chr-c50="" class="w-full sm:w-[28%] flex flex-col gap-4 snipcss0-2-12-44 snip-div">
		<h2 _ngcontent-chr-c50="" class="font-bold snipcss0-3-44-45 snip-h2">
		  Our Office Address
		</h2>
		<div _ngcontent-chr-c50="" class="flex flex-col gap-4 text-xs xl:text-base snipcss0-3-44-46 snip-div">
		  <div _ngcontent-chr-c50="" class="text-semibold snipcss0-4-46-47 snip-div">
			Headquarters
		  </div>
		  <div _ngcontent-chr-c50="" class="text-sm snipcss0-4-46-48 snip-div">
			Shop-01 Arihant Avenue SN-78/26 Wanwadi Divya Nagar Pune Pune MH 411040 IN
		  </div>
		 
		</div>
	  </div>
	</div>
	<div _ngcontent-chr-c50="" class="flex justify-between items-center mb-24 xl:mb-10 w-full xl:justify-start xl:w-[35%] xl:gap-6 xl:items-start snipcss0-1-1-53 snip-div">
	  <div _ngcontent-chr-c50="" class="w-20 snipcss0-2-53-54 snip-div">
		<h1>FincoTel</h1>
		
	  </div>
	  
	</div>
	<div _ngcontent-chr-c50="" class="text-white w-full xl:w-5/12 xl:mt-0 xl:text-base xl:mr-auto xl:text-left font-semibold text-center text-xs mt-6 pb-12 snipcss0-1-1-58 snip-div">
	  FincoTel Technology Limited © 2022 
	</div>
   
	<!---->
  </footer>


<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		/* padding: 1rem; */
		width: 100%;
		/* max-width: 1024px; */
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}



	@import url("https://fonts.googleapis.com/css?family=Poppins|Roboto"); 
@import url("https://fonts.googleapis.com/css?family=Poppins|Roboto"); 
@import url("https://fonts.googleapis.com/css?family=Poppins|Roboto"); 
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
    border-width:  0px; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
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

body { 
    margin:    0;
    font-family:   inherit; 
    line-height:  inherit;
    overflow-x: hidden; 
    scroll-behavior: smooth;
} 

@media all{ 
  body { 
    margin:    0px;
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
    text-size-adjust:   100%;
    font-family:  ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"; 
    overflow-x: hidden; 
    scroll-behavior: smooth;
  } 
}     

@media all{ 
  .bg-dark-blue { 
    --tw-bg-opacity: 1; 
    background-color: rgba(5,77,163,var(--tw-bg-opacity));
  } 
}     

@media all{ 
  .px-4 { 
    padding-left: 1rem; 
    padding-right: 1rem;
    margin-left: -.47rem;
    margin-right: -.47rem;
    margin-bottom: -.9rem;
  } 
}     

@media all{ 
  .pt-24 { 
    padding-top: 6rem;
  } 
}     

@media (min-width: 640px){ 
  .sm\:px-16 { 
    padding-left: 4rem; 
    padding-right: 4rem;
    margin-left: -0.47rem;
    margin-right: -0.47rem;
    margin-bottom: -0.9rem;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:flex { 
    display: flex;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:flex-wrap { 
    flex-wrap: wrap;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:justify-between { 
    justify-content: space-between;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:px-24 { 
    padding-left: 6rem; 
    padding-right: 6rem;
    margin-left: -.47rem;
    margin-right: -.47rem;
    margin-bottom: -.9rem;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:pb-14 { 
    padding-bottom: 3.5rem;
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
    border-width:  0px; 
    border-style:  solid; 
    border-color:  rgba(229,231,235,var(--tw-border-opacity)); 
    --tw-translate-x: 0; 
    --tw-translate-y: 0; 
    --tw-rotate: 0; 
    --tw-skew-x: 0; 
    --tw-skew-y: 0; 
    --tw-scale-x: 1; 
    --tw-scale-y: 1; 
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
  .flex { 
    display: flex;
  } 
}     

@media all{ 
  .flex-wrap { 
    flex-wrap: wrap;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:w-\[29\%\] { 
    width: 29%;
  } 
}     

@media all{ 
  .mb-24 { 
    margin-bottom: 6rem;
  } 
}     

@media all{ 
  .gap-8 { 
    gap: 2rem;
  } 
}     

@media all{ 
  .text-\[\#FEFEFE\] { 
    --tw-text-opacity: 1; 
    color: rgba(254,254,254,var(--tw-text-opacity));
  } 
}     

@media (min-width: 640px){ 
  .sm\:justify-between { 
    justify-content: space-between;
  } 
}     

@media (min-width: 640px){ 
 
}     

@media (min-width: 1280px){ 
  .xl\:mb-16 { 
    margin-bottom: 4rem;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:w-\[65\%\] { 
    width: 65%;
  } 
}     

@media all{ 
  .w-full { 
    width: 100%;
  } 
}     

@media all{ 
  .items-center { 
    align-items: center;
  } 
}     

@media all{ 
  .justify-between { 
    justify-content: space-between;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:mb-10 { 
    margin-bottom: 2.5rem;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:w-\[35\%\] { 
    width: 35%;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:items-start { 
    align-items: flex-start;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:justify-start { 
    justify-content: flex-start;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:gap-6 { 
    gap: 1.5rem;
  } 
}     

@media all{ 
  .mt-6 { 
    margin-top: 1.5rem;
  } 
}     

@media all{ 
  .pb-12 { 
    padding-bottom: 3rem;
  } 
}     

@media all{ 
  .text-center { 
    text-align: center;
  } 
}     

@media all{ 
  .text-xs { 
    font-size: 0.75rem; 
    line-height: 1rem;
  } 
}     

@media all{ 
  .font-semibold { 
    font-weight: 600;
  } 
}     

@media all{ 
  .text-white { 
    --tw-text-opacity: 1; 
    color: rgba(254,254,254,var(--tw-text-opacity));
  } 
}     

@media (min-width: 1280px){ 
  .xl\:mt-0 { 
    margin-top: 0px;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:mr-auto { 
    margin-right: auto;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:w-5\/12 { 
    width: 41.6667%;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:text-left { 
    text-align: left;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:text-base { 
    font-size: 1rem; 
    line-height: 1.5rem;
  } 
}     

@media all{ 
  button { 
    font-family:      inherit; 
    font-size:      100%; 
    line-height:  inherit; 
    margin:      0px;
    text-transform:     none;
    appearance:    button;
    background-color:   transparent; 
    background-image:   none;
    cursor:  pointer;
    padding: 0px; 
    color: inherit;
  } 
}     

@media all{ 
  .fixed { 
    position: fixed;
  } 
}     

@media all{ 
  .bottom-8 { 
    bottom: 2rem;
  } 
}     

@media all{ 
  .right-8 { 
    right: 2rem;
  } 
}     

@media all{ 
  .rounded-lg { 
    border-radius: 0.5rem;
  } 
}     

@media all{ 
  .bg-white { 
    --tw-bg-opacity: 1; 
    background-color: rgba(254,254,254,var(--tw-bg-opacity));
  } 
}     

@media all{ 
  .px-2 { 
    padding-left: 0.5rem; 
    padding-right: 0.5rem;
    margin-left: -.47rem;
    margin-right: -.47rem;
    margin-bottom: -.9rem;
  } 
}     

@media all{ 
  .py-1 { 
    padding-top: 0.25rem; 
    padding-bottom: 0.25rem;
  } 
}     

@media all{ 
  .font-bold { 
    font-weight: 700;
  } 
}     

@media all{ 
  .text-primary-blue { 
    --tw-text-opacity: 1; 
    color: rgba(1,101,254,var(--tw-text-opacity));
  } 
}     

@media all{ 
  .shadow-lg { 
    --tw-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); 
    box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),var(--tw-ring-shadow, 0 0 #0000),var(--tw-shadow);
  } 
}     

@media (min-width: 768px){ 
  .md\:bottom-20 { 
    bottom: 5rem;
  } 
}     

@media (min-width: 768px){ 
  .md\:right-24 { 
    right: 6rem;
  } 
}     

@media (min-width: 768px){ 
  .md\:py-2 { 
    padding-top: 0.5rem; 
    padding-bottom: 0.5rem;
    margin-left: -.47rem;
    margin-right: -.47rem;
    margin-bottom: -.9rem;
  } 
}     

@media (min-width: 768px){ 
  .md\:px-4 { 
    padding-left: 1rem; 
    padding-right: 1rem;
    margin-left: -.47rem;
    margin-right: -.47rem;
    margin-bottom: -.9rem;
  } 
}     

@media all{ 
  h2 { 
    margin:  0px;
    font-size: inherit; 
    font-weight: inherit;
  } 
}     

h2 { 
    cursor: auto; 
    user-select: text !important;
} 

@media (min-width: 1280px){ 
  .xl\:text-xl { 
    font-size: 1.25rem; 
    line-height: 1.75rem;
  } 
}     

h2[_ngcontent-chr-c50] { 
    font-family: Goldplay-600;
} 

@media all{ 
  .mt-8 { 
    margin-top: 2rem;
  } 
}     

@media all{ 
  .flex-col { 
    flex-direction: column;
  } 
}     

@media all{ 
  .w-5\/12 { 
    width: 41.6667%;
  } 
}     

@media all{ 
  .gap-6 { 
    gap: 1.5rem;
  } 
}     

@media (min-width: 640px){ 
  .sm\:w-\[28\%\] { 
    width: 28%;
  } 
}     

@media all{ 
  .gap-4 { 
    gap: 1rem;
  } 
}     

@media all{ 
  .w-20 { 
    width: 5rem;
  } 
}     

[_nghost-chr-c9] { 
    display: inline-block; 
    fill: none; 
    height: 24px; 
    stroke: currentColor; 
    stroke-linecap: round; 
    stroke-linejoin: round; 
    stroke-width: 2px; 
    width: 24px;
} 

@media (min-width: 640px){ 
  .sm\:w-6\/12 { 
    width: 50%;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:w-8\/12 { 
    width: 66.6667%;
  } 
}     

@media all{ 
  .mt-4 { 
    margin-top: 1rem;
  } 
}     

@media all{ 
  .max-w-\[110px\] { 
    max-width: 110px;
  } 
}     

@media all{ 
  .gap-2 { 
    gap: 0.5rem;
  } 
}     

@media all{ 
  .bg-primary-blue { 
    --tw-bg-opacity: 1; 
    background-color: rgba(1,101,254,var(--tw-bg-opacity));
  } 
}     

@media all{ 
  .py-2 { 
    padding-top: 0.5rem; 
    padding-bottom: 0.5rem;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:max-w-\[120px\] { 
    max-width: 120px;
  } 
}     

@media (min-width: 1280px){ 
  .xl\:text-lg { 
    font-size: 1.125rem; 
    line-height: 1.75rem;
  } 
}     

@media all{ 
  ul { 
    list-style: none; 
    margin: 0px; 
    padding: 0px;
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
  svg { 
    display: block; 
    vertical-align: middle;
  } 
}     

span { 
    user-select: text !important;
} 

.sr-only { 
    border:  0; 
    clip:  rect(0,0,0,0); 
    height:  1px; 
    margin:  -1px; 
    overflow:  hidden; 
    padding:  0; 
    position:  absolute; 
    width:  1px; 
    white-space: nowrap; 
    border-width: 0;
} 

@media all{ 
  .sr-only { 
    position: absolute; 
    width: 1px; 
    height: 1px; 
    padding: 0px; 
    margin: -1px; 
    overflow: hidden; 
    clip: rect(0px, 0px, 0px, 0px); 
    white-space: nowrap; 
    border-width: 0px;
  } 
}     

@media all{ 
  input { 
    font-family:  inherit; 
    font-size:  100%; 
    line-height:  inherit; 
    margin:  0px;
    padding: 0px; 
    color: inherit;
  } 
}     

@media all{ 
  .bg-white\/30 { 
    background-color: rgba(254, 254, 254, 0.3);
  } 
}     

@media all{ 
  .p-6 { 
    padding: 1.5rem;
  } 
}     

@media all{ 
  .py-4 { 
    padding-top: 1rem; 
    padding-bottom: 1rem;
  } 
}     

@media all{ 
  .ring-light-blue { 
    --tw-ring-opacity: 1; 
  } 
}     

@media all{ 
  .text-sm { 
    font-size: 0.875rem; 
    line-height: 1.25rem;
  } 
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

h1{
  color:white;
}







/* header */


header {
		display: flex;
		justify-content: space-between;
	}
  .mob-view-logo{
    padding-bottom: 20px;
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

input::placeholder{
	color : white;
}

</style>
