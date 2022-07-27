<template>
<div class="tablestat">
    <div class="tablestat__content">
        <table class="tablestat__table table">
            <tr class="table__tr">
                <th class="table__cell table__cell_th">Name</th>
                <th class="table__cell table__cell_th">Project</th>
                <th class="table__cell table__cell_th">Area</th>
                <th class="table__cell table__cell_th">Status</th>
                <th class="table__cell table__cell_th">Country</th>
            </tr>
            <!-- eslint-disable-next-line -->
            <tr class="table__tr" v-for="row in data">
                <td class="table__cell">{{ row.name }}</td>
                <td class="table__cell">{{ row.project }}</td>
                <td class="table__cell">{{ row.area }}</td>
                <td class="table__cell">{{ row.status }}</td>
                <td class="table__cell">{{ row.country }}</td>
            </tr>
        </table>
    </div>
</div>
</template>

<script>
export default {
  name: 'TableView',
  props: ['data'],
};
</script>

<style scoped lang="scss">
.tablestat {
    &__content {
    }
    &__table {
    }
}
.table {
    border: 1px solid #36434E;
    border-radius: 8px;
    table-layout: fixed;
    border-collapse: collapse;
    &__tr {
        font-family: 'Inter';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 24px;
        color: #FFFFFF;
        text-align: left;
    }
    &__cell {
        width: 180px;
        height: 55.93px;
        background: #001D31;
        border-width: 0px 1px 1px 0px;
        border-style: solid;
        border-color: #36434E;
        padding-left: 16px;
        &_th {
            background: #011625;
            font-weight: 600;
        }
    }
}
</style>
