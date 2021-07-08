<template>
    <div class="card text-center m-3">
        <h3 class="card-header">Vue.js Pagination Tutorial & Example</h3>
        <div class="card-body">
            <div v-for="item in pageOfItems" :key="item.id">{{item.name}}</div>
        </div>
        <div class="card-footer pb-0 pt-3">
            <jw-pagination :items="exampleItems" @changePage="onChangePage">
                <h1>sfdsdsfdsfsdsfsdff</h1>
                <h1>sfdsdsfdsfsdsfsdff</h1>
                <h1>sfdsdsfdsfsdsfsdff</h1>
                <h1>sfdsdsfdsfsdsfsdff</h1>
                <h1>sfdsdsfdsfsdsfsdff</h1>
            </jw-pagination>
        </div>
    </div>
</template>
<script>
// an example array of items to be paged
const exampleItems = [...Array(20).keys()].map(i => ({ id: (i+1), name: 'Item ' + (i+1) }));

export default {
    data() {
        return {
            exampleItems,
            pageOfItems: []
        };
    },
    methods: {
        onChangePage(pageOfItems) {
            // update page of items
            this.pageOfItems = pageOfItems;
        }
    }
};
</script>
