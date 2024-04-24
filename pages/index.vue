<template>


    <div>
        <NavBar />
        <SocialLinks />
        <v-lazy :min-height="200" :options="{ 'threshold': 0.5 }" transition="fade-transition">
            <About class="mt-16" />
        </v-lazy>
        <v-lazy :min-height="200" :options="{ 'threshold': 0.5 }" transition="fade-transition">
            <SkillsExperienceEducation class="mt-16" />
        </v-lazy>
        <v-lazy :min-height="200" :options="{ 'threshold': 0.5 }" transition="fade-transition">
            <MyServices class="mt-16" />
        </v-lazy>
        <v-lazy :min-height="200" :options="{ 'threshold': 0.5 }" transition="fade-transition">
            <MyPortfolio class="mt-16" />
        </v-lazy>
        <ScrollToTopButton class="z-10 cursor-pointer" />
    </div>
</template>1
