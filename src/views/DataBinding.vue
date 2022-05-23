<template>
    <h1>Hello, {{title}}</h1>
    <h1>{{htmlString}}</h1>
    <h1 v-html="htmlString"></h1>
    <div>
        <input type="text" v-model="valueModel" /><br>
        <input type="number" v-model.number="numberModel" /><br>
        <textarea v-model="message"></textarea><br>
        <select v-model="city">
            <option value="02">서울</option>
            <option value="03">담양</option>
            <option value="04">제주</option>
        </select>
        <br>
        <label><input type="checkbox" v-model="checked" true-value="yes" false-value="no">{{checked}}</label> <!-- ?? -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: 'World',
            htmlString: '<p style="color:red;">This is a red string</p>',
            valueModel: 'SouthKorea',
            numberModel: 3,
            message: 'This is a message.',
            city: '04',
            checked: true
        };
    }
}
</script>