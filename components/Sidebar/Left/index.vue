<template>
    <div class='flex flex-col h-screen'>

        <div class="p-2 my-2 hover:bg-blue-50 rounded-full w-min dark:hover:bg-white/20" :class='defaultTransition'>
            <nuxt-link to="/">
                <div class='w-8 h-8'>
                    <LogoTwitter />
                </div>
            </nuxt-link>
        </div>
        <div class="mt-2 space-y-8 ">

            <SidebarLeftTap>
                <template v-slot:icon>
                    <HomeIcon />
                </template>
                <template v-slot:title>
                    Home
                </template>
            </SidebarLeftTap>
            <SidebarLeftTap>
                <template v-slot:icon>
                    <HashtagIcon />
                </template>
                <template v-slot:title>
                    Explor
                </template>
            </SidebarLeftTap>
            <SidebarLeftTap>
                <template v-slot:icon>
                    <BellIcon />
                </template>
                <template v-slot:title>
                    Notifications
                </template>
            </SidebarLeftTap>
            <SidebarLeftTap>
                <template v-slot:icon>
                    <InboxInIcon />
                </template>
                <template v-slot:title>
                    BookMarks
                </template>
            </SidebarLeftTap>
            <SidebarLeftTap>
                <template v-slot:icon>
                    <BookmarkIcon />
                </template>
                <template v-slot:title>
                    Messages
                </template>
            </SidebarLeftTap>
            <SidebarLeftTap>
                <template v-slot:icon>
                    <DocumentTextIcon />
                </template>
                <template v-slot:title>
                    Lists
                </template>
            </SidebarLeftTap>
            <SidebarLeftTap>
                <template v-slot:icon>
                    <UserIcon />
                </template>
                <template v-slot:title>
                    Profile
                </template>
            </SidebarLeftTap>
            <SidebarLeftTap>
                <template v-slot:icon>
                    <DotsCircleHorizontalIcon />
                </template>
                <template v-slot:title>
                    More
                </template>
            </SidebarLeftTap>
        </div>
    </div>
</template>
<script setup>
import { HomeIcon } from '@heroicons/vue/solid';
import {HashtagIcon ,BellIcon,InboxInIcon ,BookmarkIcon,DocumentTextIcon,UserIcon,DotsCircleHorizontalIcon } from '@heroicons/vue/outline';
const { defaultTransition } = useTailwindConfig();

</script>