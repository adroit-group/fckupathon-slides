/** * QRCode Component * * Renders a QR code as an SVG using qrcode.vue. * *
@example *
<QRCode value="https://example.com" :size="200" />
*/
<template>
  <qrcode-vue
    :value="value"
    :size="size"
    :margin="margin"
    :level="level"
    render-as="svg"
  />
</template>

<script setup lang="ts">
import QrcodeVue from "qrcode.vue"

/** Error correction level for QR codes */
type ErrorCorrectionLevel = "L" | "M" | "Q" | "H"

interface Props {
  /** The data to encode in the QR code */
  value?: string
  /** The size of the QR code in pixels */
  size?: number
  /** The margin around the QR code */
  margin?: number
  /** Error correction level */
  level?: ErrorCorrectionLevel
}

const props = withDefaults(defineProps<Props>(), {
  value: "https://adroitgroup.io",
  size: 300,
  margin: 3,
  level: "L",
})
</script>
