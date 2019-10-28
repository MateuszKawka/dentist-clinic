<template>
  <section class="section pricing" id="pricing">
    <h2 class="section__title">Pricing</h2>
    <PricingItem v-for="item in pricing" :key="item.name" :offer="item"/>
  </section>
</template>

<script>
import PricingItem from '@/components/PricingItem'
export default {
  name: 'Pricing',
  components: {
    PricingItem
  },
  data() {
    return {
      pricing: [
        {
          name: 'General Dentistry',
          values: [
            {
              name: 'New patient consultation adult (first visit to the practice, includes all x-rays and panoramic x-ray if required)',
              price: 97
            },
            {
              name: 'Check up (existing patients, includes all necessary small x-rays)',
              price: 59
            },
            {
              name: `Children's consultation`,
              price: 40
            },
            {
              name: `Extractions`,
              price: 92
            }
            ,
            {
              name: `Root canal (with a general dentist)`,
              price: 339
            }
            
          ]
        },
        {
          name: 'Dental Hygiene',
          values: [
            {
              name: 'New patient hygiene treatment',
              price: 82
            },
            {
              name: 'Routine hygiene treatment',
              price: 82
            },
            {
              name: 'Complex clean (intensive stain and heavy plaque removal)',
              price: 123
            },
            {
              name: 'Orthodontic maintenance programme',
              price: 82
            },
            {
              name: `Children's hygiene treatment`,
              price: 62
            }
          ]
        },
        {
          name: 'Restorative Dentistry',
          values: [
            {
              name: 'Tooth coloured fillings (depending on complexity)',
              price: 91
            },
            {
              name: 'Crowns (depending on material and complexity)',
              price: 729
            },
            {
              name: 'Bridge (depending on material and complexity)',
              price: 760
            }
          ]
        },
        {
          name: 'Cosmetic Dentistry',
          values: [
            {
              name: 'Professional home tooth whitening',
              price: 317
            },
            {
              name: 'Composite Bondingfrom',
              price: 152
            },
            {
              name: 'Composite Veneersfrom',
              price: 215
            },
            {
              name: 'Porcelain Veneersfrom',
              price: 760
            },
            {
              name: 'Treatment of White Spots',
              price: 300
            }
          ]
        },
        {
          name: 'Orthodontics',
          values: [
            {
              name: 'Orthodontic consultation with specialist',
              price: 128
            },
            {
              name: 'Invisalign',
              price: 1500
            },
            {
              name: 'Labial (Outside) Braces',
              price: 2000
            },
            {
              name: 'Labial (Inside) Braces',
              price: 5500
            },
            {
              name: 'Retainers',
              price: 180
            }
          ]
        },
        {
          name: 'Advanced Dentistry',
          values: [
            {
              name: 'Periodontic consultation (includes panoramic x-ray',
              price: 135
            },
            {
              name: 'Implant consultation (includes 3D scan)',
              price: 158
            },
            {
              name: 'Single restored implant',
              price: 3000
            },
            {
              name: 'Root Canal (with an Endodontist)',
              price: 569
            }
          ]
        }
      ]
    }
  }
}
</script>