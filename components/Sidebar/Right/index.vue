<template>
    <div class='flex flex-col'>

        <!-- Preview Card : What's happening -->
        <SidebarRightPreviewCard  title="What's happening">
            <SidebarRightPreviewCardItem v-for='whatHappening in WhatsHappening' :key='whatHappening.title'>
                <div>
                    <h2 class='font-bold text-gray-800 text-md dark:text-white'>
                        {{ whatHappening.title }}
                    </h2>
                    <p class='text-xs text-gray-400'>
                        {{ whatHappening.count }}
                    </p>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>

        <!-- Preview Card : Who to follow -->
        <SidebarRightPreviewCard  title="Who to follow">
            <SidebarRightPreviewCardItem v-for='whoToFollow in whoToFollowItems' :key='whoToFollow.title'>
                <div class='flex flex-row justify-between  items-center p-2 '>
                    <div class='flex flex-row'>
                        <img 
                            :src='whoToFollow.image' 
                            :alt='whoToFollow.name'
                            class='w-10 h-10 rounded-full' />
                        <div class='ml-2 flex flex-col'>
                            <h1 class='text-sm font-semibold text-gray-900 dark:text-white'>
                                {{ whoToFollow.name }}
                            </h1>
                            <p class='text-xs text-gray-400'>
                                {{ whoToFollow.handle }}
                            </p>
                        </div>
                    </div>
                    <div class='flex h-full'>
                        <button class='px-4 py-2 text-xs font-bold rounded-full bg-black text-white dark:text-black dark:bg-white'>Follow</button>
                    </div>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>


    </div>
</template>

<script setup>
const WhatsHappening = ref([
    {
        title: 'SpaceX',
        count: '18.8k Tweets',
    },
    {
        title: '#Cooding Fun',
        count: '8.8k Tweets',
    },
    {
        title: '#Artforall',
        count: '1.8k Tweets',
    },
])

const whoToFollowItems = ref([
    {
        name: 'John Doe',
        handle: '@johndoe',
        image: 'https://picsum.photos/id/10/200/200',
        // image: 'https://picsum.photos/200/200',
    },
    {
        name: 'John Doe',
        handle: '@johndoe',
        // image: 'https://picsum.photos/id/10/200/200',
        image: 'https://picsum.photos/200/200',
    },
    
])
</script>