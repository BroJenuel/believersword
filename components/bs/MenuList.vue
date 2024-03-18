<script setup lang="ts">
const props = defineProps({
    title: String,
});
</script>

<template>
    <li>
        <NavigationMenuLink as-child>
            <a
                v-bind="$attrs"
                class="block select-none space-y-1 rounded-md p-3 leading-none no-underline outline-none transition-colors hover:bg-accent hover:text-accent-foreground focus:bg-accent focus:text-accent-foreground"
            >
                <div class="text-green-300 mb-[5px] font-medium leading-[1.2]">
                    {{ props.title }}
                </div>
                <p class="text-sm my-0 leading-[1.4]">
                    <slot />
                </p>
            </a>
        </NavigationMenuLink>
    </li>
</template>
