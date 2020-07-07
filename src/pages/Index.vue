<template>
  <Layout>
    <div class="hero container-inner mx-auto flex flex-col sm:flex-row justify-between py-16">
      <div class="text-4xl font-bold w-full sm:w-3/5 text-center sm:text-left">
        <div class="leading-tight">{{ $static.metadata.siteName }}</div>
        <div class="text-blue-700 leading-tight">Tax Preparation services</div>
      </div>
    </div> <!-- end hero -->

    <div class="container-inner mx-auto">
      <p class="text-lg sm:text-xl">Straight-forward tax preparation for personal and sole proprietorship clients.  Let us help you complete and file your income taxes through our personal service. We will clarify the annual changes from <a href="https://www.canada.ca/en/revenue-agency.html">Canada Revenue Agency</a> and consider how it affects your personal taxes.</p>

      <div class="flex justify-between items-center py-6">
        <div class="w-full sm:w-1/2 px-8 py-8 sm:py-0">
          <g-image src="../../static/undraw_spreadsheet_69ax.svg" alt="spreadsheet" />
        </div>
        <div class="w-1/2 px-8 hidden sm:flex justify-end">
          <g-image src="../../static/undraw_attached_file_n4wm.svg" alt="file" />
        </div>
      </div>
    </div>

    <div class="overflow-x-hidden">
      <div class="notes container-inner mx-auto text-xl border-t border-gray-500 border-b py-16 mb-16 relative">
        <h2 class="font-bold mb-6" id="notes">Here are some things to note:</h2>

        <ul class="text-lg sm:text-xl space-y-6">
          <li class="checkmark">
            <div>Office Hours</div>
            <div class="text-lg text-gray-600">From January 15th -April 30th 2020, our office hours are 9:00am to 5:00pm. After April 30th, 2020, by appointment only.</div>
          </li>
          <li class="checkmark">
            <div>Focus on you</div>
            <div class="text-lg text-gray-600">Please do not call outside these hours; we need to focus time to work on your returns.</div>
          </li>
          <li class="checkmark">
            <div>Filing Deadline</div>
            <div class="text-lg text-gray-600">Our deadline to accept taxes is Saturday, April 27th 2020.  This gives us time to prepare, sign nd send in last-minute returns to CRA.</div>
          </li>
          <li class="checkmark">
            <div>Project Four</div>
            <div class="text-lg text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui ab nam animi iure nemo exercitationem a, eius non culpa itaque!</div>
          </li>

        </ul>
      </div> <!-- end notes -->
    </div>

    <div class="overflow-x-hidden border-gray-200 border-b">
      <div class="get-to-know-me container-inner mx-auto text-xl pb-16 relative">
        <h2 class="font-bold mb-6" id="about">Get to know KTC Taxes:</h2>


        <div class="flex flex-col sm:flex-row justify-between items-center mb-16">
          <div><g-image src="../../static/avatar.jpg" alt="avatar" class="w-32 h-32 rounded-full mb-8 lg:mb-0" /></div>
          <div class="flex-1 text-lg sm:text-xl ml-6">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eum quae architecto minus molestias iusto ducimus fuga quo quia libero dignissimos, fugiat modi assumenda debitis laboriosam.</div>
        </div>

      </div> <!-- end get-to-know me -->
    </div>

    <div class="overflow-x-hidden">
      <div class="contact-me bg-background-secondary pt-16">
        <div class="container-inner mx-auto text-xl pb-4 relative">
          <h2 class="font-bold mb-6" id="contact">Contact me:</h2>

          <p class="mb-12">Static sites cannot submit forms on their own. However, services like <a href="https://www.netlify.com/docs/form-handling">Netlify Forms</a> or <a href="https://formspree.io">FormSpree</a> can help you do this without a backend.</p>

          <div class="text-lg sm:text-lg mb-16">
            <form action="#" class="mb-12">
              <div class="flex flex-wrap mb-6 -mx-4">
                  <div class="w-full md:w-1/2 mb-6 md:mb-0 px-4">
                      <label class="block mb-2 text-copy-primary" for="name">
                          Name
                      </label>

                      <input type="text" name="name" id="name" placeholder="Firstname Surname" class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-blue-700 mb-2 p-4" required>
                  </div>

                  <div class="w-full px-4 md:w-1/2">
                      <label class="block text-copy-primary mb-2" for="email">
                          Email Address
                      </label>

                      <input type="email" name="email" id="email" placeholder="email@example.com"  class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-blue-700 mb-2 p-4" required>
                  </div>
              </div>

              <div class="w-full mb-12">
                  <label class="block text-copy-primary mb-2" for="message">
                      Message
                  </label>

                  <textarea id="message" rows="5" name="message" class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none appearance-none focus:border-blue-700 mb-2 px-4 py-4" placeholder="Enter your message here." required></textarea>
              </div>

              <div class="flex justify-end w-full">
                  <input type="submit" value="Submit" class="block bg-blue-700 hover:bg-blue-800 text-white text-sm font-semibold tracking-wide uppercase shadow rounded cursor-pointer px-6 py-3">
              </div>
          </form>
          </div>
        </div>
      </div> <!-- end contact-me -->
    </div>

    <div class="newsletter bg-background-tertiary">
      <div class="container-inner mx-auto py-16 pb-8 text-center textl-xl">
        <h2 class="text-2xl font-bold mb-8">Join my Newsletter</h2>

        <div class="w-4/5 mx-auto mb-8">
          <p class="mb-8 text-lg sm:text-xl">Stay notified of important information via tidbits and "The Checklist"</p>

          <form action="#">
            <div class="flex flex-col sm:flex-row">
              <input type="email" name="email" placeholder="Your email address" class="flex-1 bg-background-form rounded sm:rounded-r-none px-4 py-4 leading-normal border border-border-color-primary sm:border-r-0 shadow outline-none focus:border-blue-700 z-10" required>
              <button data-element="submit" class="flex-2 w-40 uppercase bg-blue-700 text-white rounded sm:rounded-l-none text-lg py-3 px-8 tracking-wide shadow focus:outline-none hover:bg-blue-800 focus:bg-blue-800 z-10 w-full sm:w-auto mt-4 sm:mt-0">
                <span>Subscribe</span>
              </button>
            </div>
          </form>
        </div>
      </div>


    </div>

  </Layout>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  metaInfo: {
    title: 'Home'
  }
}
</script>

