<template>
  <div class="booking" id="booking">
    <div class="form-container">
      <p class="form-container__paragraph">111 - 111 - 111</p>
      <p class="form-container__paragraph">dentist@clinic.atlantic</p>
      <form class="form">
        <label for="name" class="form__label">Name</label>
        <input type="text" id="name" class="form__input" />
        <label for="phone" class="form__label">Phone</label>
        <input type="text" id="phone" class="form__input" />
        <label for="note" class="form__label">Note</label>
        <textarea type="text" id="note" class="form__textarea"></textarea>
        <label for="date" class="form__label">Date</label>
        <client-only>
          <DatePicker :lang="lang" v-model="date"  type="datetime" :time-picker-options="timePickerOptions" 
          format="YYYY-MM-DD hh:mm:ss a" placeholder="Select Time" confirm :popupStyle="popupStyle" />
        </client-only>
        <button type="button" class="button button--form">Send</button>
      </form>
    </div>
  </div>
</template>

<script >
export default {
  name: 'Booking',
  data() {
    return {
      date: '',
      lang: {
        days: ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'],
        months: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
        pickers: ['next 7 days', 'next 30 days', 'previous 7 days', 'previous 30 days'],
        placeholder: {
          date: 'Select Date',
          dateRange: 'Select Date Range'
        }
      },
      timePickerOptions: {
        start: '08:00',
        step: '01:00',
        end: '19:00'
      },
      popupStyle: {
        color: 'red'
      }
    }
    }
  }
</script>