<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import Welcome from '@/Components/Welcome.vue';

defineProps({
    users: {
        type: Array,
        default: () => [],
    },
});
</script>

<template>
    <AppLayout title="Users">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight">
                Users
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white dark:bg-gray-800 overflow-hidden shadow-xl sm:rounded-lg">
                    <!-- <pre>{{ users }}</pre> -->
                    <div v-for="user in users" :key="user.id">
                        {{ user.name }}
                    </div>
                </div>
            </div>
        </div>
    </AppLayout>
</template>
