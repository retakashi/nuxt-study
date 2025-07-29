<script setup lang="ts">
const props = defineProps<{
    title: string;
    description?: string;
}>();
</script>

<template>
    <Card>
        <CardHeader>
          <CardTitle>{{ title }}</CardTitle>
          <CardDescription>{{ description }}</CardDescription>
        </CardHeader>
    </Card>
</template>