<script setup lang="ts">
import { Head } from '@inertiajs/vue3';
import PlaceholderPattern from '@/components/PlaceholderPattern.vue';
import { dashboard } from '@/routes';

defineOptions({
    layout: {
        breadcrumbs: [
            {
                title: 'Dashboard',
                href: dashboard(),
            },
        ],
    },
});
</script>

<template>
    <Head title="Dashboard" />

    <div
        class="flex h-full flex-1 flex-col gap-4 overflow-x-auto rounded-xl p-4"
    >
        <section
            class="rounded-xl border border-sidebar-border/70 bg-card p-6 text-card-foreground shadow-sm dark:border-sidebar-border"
        >
            <div class="flex flex-col gap-2">
                <p class="text-sm font-medium text-red-500">
                    Bienvenido a LaraCode
                </p>
                <h1 class="text-2xl font-semibold tracking-tight">
                    Hola, {{ $page.props.auth.user.name }}
                </h1>
                <p class="max-w-2xl text-sm text-muted-foreground">
                    Aquí podrás continuar tus cursos y consultar tu progreso.
                </p>
            </div>
        </section>
        <div class="grid auto-rows-min gap-4 md:grid-cols-3">
            <div
                class="relative aspect-video overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border"
            >
                <PlaceholderPattern />
            </div>
            <div
                class="relative aspect-video overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border"
            >
                <PlaceholderPattern />
            </div>
            <div
                class="relative aspect-video overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border"
            >
                <PlaceholderPattern />
            </div>
        </div>
        <div
            class="relative min-h-[100vh] flex-1 rounded-xl border border-sidebar-border/70 md:min-h-min dark:border-sidebar-border"
        >
            <PlaceholderPattern />
        </div>
    </div>
</template>
