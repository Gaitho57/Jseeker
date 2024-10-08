<script>
import { ref } from 'vue'
import { ClipboardDocumentCheckIcon } from '@heroicons/vue/24/outline'
// Or if you prefer solid icons:
// import { ClipboardDocumentCheckIcon } from '@heroicons/vue/24/solid'
import { CalendarIcon } from '@heroicons/vue/24/outline'
import { BellIcon } from '@heroicons/vue/24/outline'
import { ChartLineIcon } from '@heroicons/vue/24/outline'
import { HandshakeIcon } from '@heroicons/vue/24/solid'
import { DocumentIcon } from '@heroicons/vue/24/outline'
import { CogIcon } from '@heroicons/vue/24/outline'

export default {
  setup() {
    const featureImage = ref(FeatureImage)
    
    return {
      featureImage
    }
  },
  data () {
    return {
        features :[
            {
                Icon: ClipboardDocumentCheckIcon,
                Title: 'Effortless Application Entry',
                Description: 'Save time by easily adding jobs with copy-paste functionality.',
                Learn_More: 'Discover how our intuitive interface lets you capture job details in '
            },
            {
                Icon: CalendarIcon,
                Title: 'Stay Organized with All-in-One Tracking',
                Description: 'Manage application stages (applied, planned, interview reminders) and never miss a step',
                Learn_More: 'See how our app simplifies your job search journey by keeping track of applications, interview dates, and critical milestones in one place'
            },
            {
                Icon: BellIcon,
                Title: 'Be Prepared & Never Miss an Interview',
                Description: 'Set reminders for upcoming interviews and store valuable feedback to improve your performance',
                Learn_More: 'Get notified about upcoming interviews and capture feedback received to refine your approach and land your dream job Our app also offers interview tips and tools to help you feel confident and prepared'
            },
            {
                Icon: ChartLineIcon,
                Title: 'Gain Valuable Insights from Your Data',
                Description: 'Analyze application trends, success rates, and identify areas for improvement',
                Learn_More: ' Leverage insightful data visualizations to understand your application performance, identify patterns, and track progress towards your job search goals. Our app empowers you to make data-driven decisions and optimize your approach '
            },
            {
                Icon: 'Two connected squares representing job boards and your app',
                Title: ' Seamless Job Discovery & Application',
                Description: 'Import relevant job postings directly from popular job boards (coming soon)',
                Learn_More: ' Stay ahead of the game by directly importing job openings from popular job boards within our app (coming soon). This saves time and ensures you are applying to the most relevant positions'
            },
            {
                Icon: HandshakeIcon,
                Title: 'Get Feedback & Boost Your Applications',
                Description: 'Share applications with mentors for valuable insights (coming soon)',
                Learn_More: ' Gain an edge in the competitive job market by collaborating with mentors or career advisors through our secure platform (coming soon). Share applications and receive valuable feedback to strengthen your application package '
            },
            {
                Icon: DocumentIcon,
                Title: 'Craft Compelling Application Materials',
                Description: 'Create personalized resumes and cover letters that impress employers (coming soon)',
                Learn_More: ' Build winning applications with our resume and cover letter builder (coming soon). Utilize our templates, prompts, and editing tools to create customized documents that showcase your skills and experience effectively '
            },
            {
                Icon: CogIcon,
                Title: 'Personalize Your Job Search Experience',
                Description: ' Tailor notification preferences and dashboard views to fit your needs (coming soon)',
                Learn_More: ' Take control of your job search experience. Customize notification preferences to receive relevant updates and personalize your dashboard layout to prioritize the information that matters most to you (coming soon) '
            },
        ],
    }
},
}
</script>

<template>
<section>
<div class="flex justify-center"> 
<h1 class="text-2xl font-bold text-gray-800 mb-4 ">Manage & Track Applications Like a Pro</h1>
</div>

<div class="container mx-auto px-4">
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
<div v-for="(feature, index) in features" :key="index" class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
    <component :is="feature.Icon" class="h-8 w-8 text-blue-500 mb-4" />
    <div class="p-5">
        <h1>
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ feature.Title }}</h5>
        </h1>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{{ feature.Description }}</p>
        <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
            Read more
             <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
            </svg>
        </a>
    </div>
</div>
</div>
</div>

</section>
</template>

