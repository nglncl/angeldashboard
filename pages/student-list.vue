<template>
    <v-card>
        <v-card-title>
            Students List Page
            <v-spacer></v-spacer>
            <v-text-field v-model="search" append-icon="mdi-magnify" label="Search" single-line
                hide-details></v-text-field>
        </v-card-title>
        <v-data-table :headers="headers" :items="StudentData" :search="search">
            <template slot="item.actions" slot-scope="{item}">
                <v-btn color="green accent-4"> DELETE</v-btn>
                <v-btn color="red accent-4"> EDIT</v-btn>
            </template>
        </v-data-table>

    </v-card>
</template>
<script>
export default {
    data() {
        return {
            search: '',
            headers: [
                {
                    text: 'ID',
                    align: 'start',
                    sortable: false,
                    value: 'StudentID',
                },
                { text: 'First Name', value: 'First_Name' },
                { text: 'Last Name', value: 'Last_Name' },
                { text: 'Middle Initial', value: 'Middle_Initial' },
                { text: 'Course', value: 'Course' },
                { text: 'Year', value: 'Year' },
                { text: '', value: "actions" }
            ],
            StudentData: [
             

            ],
        }
    },
}
</script>