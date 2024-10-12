<template>
  <main>
    <div id="header">
      <h1>Weekly schedule</h1>
    </div>
    <div id="table">
      <table>
        <thead>
          <tr id="table-header">
            <th colspan="2"><a class="calender-header-button" href="#">Select Month/Year</a></th>
            <th class="current-year-month" colspan="3">{{ currentMonthYear }}</th>
            <th colspan="2"><a class="calender-header-button" href="#">Add Event</a></th>
          </tr>
          <tr id="months">
            <th>Monday</th>
            <th>Tuesday</th>
            <th>Wednesday</th>
            <th>Thursday</th>
            <th>Friday</th>
            <th>Saturday</th>
            <th>Sunday</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(week, index) in days" :key="index">
            <td v-for="day in week" :key="day.date" :class="{ empty: !day.date }">
              <div class="date">{{ day.date }}</div>
              <div class="slot-data" v-for="slot in day.slots" :key="slot.time">
                <a class="data-link">{{ slot.time }}</a>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      currentDate: new Date(), // Stores the current date
      days: this.generateDaysForMonth(new Date().getFullYear(), new Date().getMonth())
    }
  },
  computed: {
    currentMonthYear() {
      return this.currentDate.toLocaleDateString('en-US', {
        year: 'numeric',
        month: 'long'
      })
    }
  },
  methods: {
    generateDaysForMonth(year, month) {
      const daysInMonth = new Date(year, month + 1, 0).getDate()
      const firstDayOfMonth = new Date(year, month, 1).getDay()

      // Adjust starting index for Monday (0: Monday, ..., 6: Sunday)
      const startOffset = (firstDayOfMonth + 6) % 7

      let weeks = []
      let week = Array(startOffset).fill({ date: '', slots: [] })

      for (let day = 1; day <= daysInMonth; day++) {
        const date = new Date(year, month, day)

        week.push({
          date: date.getDate(), // Only the day number
          slots: [
            { time: '9:00 AM' },
            { time: '12:00 PM' },
            { time: '3:00 PM' },
            { time: '5:00 PM' }
          ] // Modify as needed for different time slots
        })

        // Push and reset the week array when it's filled
        if (week.length === 7) {
          weeks.push(week)
          week = []
        }
      }

      // Push any remaining days in the last week
      if (week.length > 0) {
        // Fill the rest with empty days
        while (week.length < 7) {
          week.push({ date: '', slots: [] })
        }
        weeks.push(week)
      }

      return weeks
    }
  }
}
</script>

<style scoped>
main {
  width: 90%;
  display: flex;
  justify-content: flex-start;
  flex-direction: column;
}

#table {
  width: 99%;
  margin: 10px auto;
  box-shadow: var(--shadow);
  height: 100%;
  max-height: 90vh;
  overflow-y: scroll;
}

#table table {
  border-collapse: collapse;
  border-spacing: 0 20px;
  table-layout: fixed;
  width: 100%;
  height: 100%;
  text-align: center;
}

#table th {
  padding: 20px;
  color: var(--fill);
  font-weight: bold;
}

.current-year-month {
  font-weight: bold;
  border-bottom: 2px solid var(--underline);
  box-shadow: var(--shadow);
}

.calender-header-button {
  padding: 10px;
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  transition: background-color 0.5s ease;
  background-color: var(--primary);
  color: var(--text-color);
}

.calender-header-button:hover {
  background-color: var(--hover);
}

td {
  border: 1px solid var(--fill);
  text-align: center;
  padding: 20px;
  text-align: right;
  vertical-align: top;
  background-color: var(--mini-background);
}

td:not(.empty):hover {
  transform: scale(1.1);
  border-radius: var(--radius);
}

td.empty {
  background-color: var(--primary);
  cursor: default;
}

td .date {
  text-align: left;
  margin-bottom: 10px;
}

.slot-data {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 5% auto;
  width: 100%;
}

.data-link {
  width: 100%;
  text-align: center;
  border-radius: var(--radius);
  box-shadow: var(--hshadow);
}

.data-link:hover {
  background-color: var(--hover);
}
</style>
