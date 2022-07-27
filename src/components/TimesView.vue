<template>
<div class="time">
    <div class="time__content">
        <div class="time__title">{{ title }}</div>
        <div class="time__description">{{ description }}</div>
    </div>
</div>
</template>

<script>
export default {
  name: 'TimesView',
  props: ['title', 'description'],
};
</script>

<style scoped lang="scss">
.time {
    &__content {
        width: 273px;
        height: 128px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 7px;
        font-family: 'Inter';
        font-style: normal;
        color: #FFFFFF;
        background: #001D31;
        border: 1px solid #36434E;
        border-radius: 8px;
    }
    &__title {
        font-weight: 600;
        font-size: 36px;
        line-height: 48px;
    }
    &__description {
        font-weight: 400;
        font-size: 16px;
        line-height: 24px;
    }
}
</style>
