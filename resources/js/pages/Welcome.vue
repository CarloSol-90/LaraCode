<script setup lang="ts">
import { Head, Link } from '@inertiajs/vue3';
import { dashboard, login, register } from '@/routes';
</script>

<template>
    <Head title="Bienvenido" />

    <div class="min-h-screen bg-white text-slate-950">
        <header
            class="absolute inset-x-0 top-0 mx-auto flex w-full max-w-7xl justify-end p-5 sm:p-8"
        >
            <nav
                aria-label="Navegación de usuario"
                class="flex items-center gap-3"
            >
                <Link
                    v-if="$page.props.auth.user"
                    :href="dashboard()"
                    class="rounded-lg bg-red-500 px-5 py-2.5 text-sm font-semibold text-white transition-colors hover:bg-red-600 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-red-500"
                >
                    Ir al panel
                </Link>

                <template v-else>
                    <Link
                        :href="login()"
                        class="rounded-lg px-4 py-2.5 text-sm font-semibold text-slate-700 transition-colors hover:bg-slate-100 hover:text-slate-950 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-red-500"
                    >
                        Iniciar sesión
                    </Link>
                    <Link
                        :href="register()"
                        class="rounded-lg bg-red-500 px-5 py-2.5 text-sm font-semibold text-white transition-colors hover:bg-red-600 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-red-500"
                    >
                        Registrarse
                    </Link>
                </template>
            </nav>
        </header>

        <main class="flex min-h-screen items-center justify-center px-6">
            <h1 class="sr-only">
                LaraCode — Aprende, practica y domina Laravel
            </h1>
            <img
                src="/images/laracode-logo.png"
                alt="LaraCode, aprende, practica y domina"
                class="h-auto w-65 object-contain sm:w-60"
            />
        </main>
    </div>
</template>
