<script>
import DrawerHead from './DrawerHead.vue'
import { ref, computed, inject } from 'vue'

const props = defineProps({
  totalPrice: Number,
  vatPrice: Number
})

const { cart, closeDrawer } = inject('cart')

const isCreating = ref(false)
const orderId = ref(null)

const createOrder = async () => {
  try {
    isCreating.value = true

    const { data } = await axios.post(`https://604781a0efa572c1.mokky.dev/orders`, {
      items: cart.value,
      totalPrice: props.totalPrice.value
    })

    cart.value = []

    orderId.value = data.id
  } catch (err) {
    console.log(err)
  } finally {
    isCreating.value = false
  }
}

const cartIsEmpty = computed(() => cart.value.length === 0)
const buttonDisabled = computed(() => isCreating.value || cartIsEmpty.value)
</script>

<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opactiy-70">
    <div class="bg-white w-96 h-full fixed right-0 z-20 top-0 p-8">
      <DrawerHead />

      <h2 class="text-xl font-bold"></h2>
    </div>
  </div>
</template>
