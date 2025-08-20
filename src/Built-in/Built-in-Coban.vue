<template>
    <h1>Built-in Components</h1>
</template>

<script setup>
    import { ref } from 'vue'

    const name = ref('')

    // Demo Console
    const message = ref('Test console.log')
    console.log(message.value)
    console.warn('Test console.warn')
    console.error('Test console.error')
    console.info('Test console.info')

    // Demo confirm
    confirm('Bạn có bằng lái xe chưa?') ? console.log('Có Bằng Rồi') : console.log('Chưa Có')

    // Demo Prompt
    const input = prompt('Nhập tên của bạn')
    if (input) {
        name.value = input
    } else {
        name.value = 'Không có tên'
    }
    console.log('Tên của bạn là:', name.value)

    // Demo setTimeout
    setTimeout(() => {
        alert('Test setTimeout 5s')
        console.log('Test setTimeout 5s')
    }, 2000)

    // Demo setInterval
    let count = 0
    const interval = setInterval(() => {
        console.log('Interval lần thứ : ' + ++count)
        if (count === 5) {
            clearInterval(interval)
            console.log('Đã dừng setInterval sau 5 lần')
        }
    }, 1000)
</script>