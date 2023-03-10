<template>  
    <div id="date-picker" v-cloak="v-cloak">
    <input type="text" v-model="showDate" @input="updatePickedDate($event.target.value)" @focus="onFocus()" @blur.prevent="onBlur()"/>
    <div class="calendar" v-show="open" @mouseDown.prevent.stop="onMouseDown()" @mouseUp.prevent.stop="onMouseUp()">
        <div class="header">
        <div class="center">
            <div class="left arrow" @click="changeCurMonth(-12)">&lt;</div>
            <div class="right arrow" @click="changeCurMonth(12)">&gt;</div>
            <div class="year">{{ curYear }}</div>
            <div class="left arrow" @click="changeCurMonth(-1)">&lt;</div>
            <div class="right arrow" @click="changeCurMonth(1)">&gt;</div>
            <div class="month">{{ curMonth | formatMonth }}</div>
        </div>
        </div>
        <table>
        <thead>
            <tr class="week">
            <td>Sun</td>
            <td>Mon</td>
            <td>Tue</td>
            <td>Wen</td>
            <td>Thu</td>
            <td>Fri</td>
            <td>Sat</td>
            </tr>
        </thead>
        <tbody>
            <tr v-for="row in rows">
            <td class="day" v-for="date in row" :class="{ 'other-month': date.getMonth() !== curMonth , 'selected': date.valueOf() == pickedDate.valueOf()}" @click="pickDate(date)">{{ date.getDate() }}</td>
            </tr>
        </tbody>
        </table>
    </div>
    </div>
</template>

<script>
    export default {
      name: "datePicker",
      data() {
        let d = new Date(2017,6,15)
        return {
        open: false,
        forceOpen: false,
        pickedDate: d,
        curYear: d.getFullYear(),
        curMonth: d.getMonth(),
        curDay: d.getDate()
        }
      },
      computed: {
            showDate: {
            get() {
                let d = this.pickedDate
                return d.getFullYear() + '-' + (d.getMonth() < 9 ? '0' + (d.getMonth() + 1) : d.getMonth()) + '-' + (d.getDate() < 10 ? '0' + d.getDate() : d.getDate())
            }
            },
            leapYear() {
            if (this.curYear % 100 === 0) {
                return this.curYear % 400 === 0
            } else {
                return this.curYear % 4 === 0
            }
            },
            dates() {
            let ret = []
            let firstDayOfMonth = new Date(this.curYear, this.curMonth, 1)
            let lastDayOfMonth = new Date(this.curYear, this.curMonth, this.getLastDayOfMonth(this.curMonth))
            ret.unshift(firstDayOfMonth)
            for (let d = this.prevDate(firstDayOfMonth); d.getDay() !== 6; d = this.prevDate(d)) {
                ret.unshift(d)
            }
            for (let d = this.nextDate(firstDayOfMonth); d <= lastDayOfMonth; d = this.nextDate(d)) {
                ret.push(d)
            }
            for (let d = this.nextDate(lastDayOfMonth); d.getDay() !== 0; d = this.nextDate(d)) {
                ret.push(d)
            }
            return ret
            },
            rows() {
            return this.dates.reduce(function(p, c, i) {
                if (i % 7 === 0) {
                p[p.length] = []
                }
                p[p.length - 1].push(c)
                return p
            }, [])
            }
      },
      methods: {
        changeCurMonth(n) {
            let temp = this.curMonth + n
            if (temp < 0) {
                this.curYear -= 1
            } else if (temp >= 12) {
                this.curYear += 1
            }
            this.curMonth = ((temp) + 12) % 12
        },
        nextDate(d) {
            let ret = new Date(d.valueOf())
            ret.setDate(d.getDate() + 1)
            return ret
        },
        prevDate(d) {
            let ret = new Date(d.valueOf())
                // console.log("old", ret.toString())
            ret.setDate(d.getDate() - 1)
                // console.log("new", ret.toString())
            return ret
        },
        getLastDayOfMonth(m) {
            let ret = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
            if (this.leapYear) {
                ret[1] = 29
            }
            return ret[m]
        },
        pickDate(d) {
            this.pickedDate = d
            this.curMonth = d.getMonth()
            this.curYear = d.getFullYear()
        },
        onFocus () {
            this.open = true
            this.forceOpen = false
        },
        onBlur () {
            this.open = this.forceOpen
        },
        onMouseDown () {
            this.forceOpen = true
        },
        onMouseUp () {
            this.forceOpen = false
        },
        updatePickedDate(v) {
            let reg = new RegExp('(\\d{4})-(\\d{2})-(\\d{2})')
            let m = reg.exec(v)
            if (m) {
                let year = parseInt(m[2])
                let month = parseInt(m[2])
                let day = parseInt(m[3])
                // 日期符合范围
                // if (month < 1900 || month < ) {
                //  return
                // }
                if (month > 12 || month < 1) {
                return
                }
                if (day < 1 || day > this.getLastDayOfMonth(month)) {
                return
                }
                this.pickedDate = new Date(m[1], parseInt(m[2]) - 1, m[3])
                this.curMonth = parseInt(m[2]) - 1
                this.curYear = parseInt(m[1])
            }
        }
      },
      filters: {
        formatMonth(m) {
            return [
                '一月',
                '二月',
                'Mar',
                'Apr',
                'May',
                'Jun',
                'Jul',
                'Aug',
                'Sep',
                'Oct',
                'Nov',
                'Dec'
            ][m]
            }
      }
    };
</script>
<style lang="scss">
#date-picker {
  display: inline-block;
}
.other-month {
  color: gray;
}
.arrow {
  cursor: pointer;
  width: 1.5em;
}
.arrow:hover {
  color: steelblue;
  font-weight: 400;
}
.year,
.month {
  height: 1.2em;
}
.left {
  float: left;
}
.right {
  float: right;
}
.center {
  text-align: center;
  clear: both;
}
table {
  clear: both;
}
table .week td {
  color: #9a9a9a;
  font-family: serif;
}
table td {
  width: 2em;
  height: 2em;
  vertical-align: middle;
  text-align: center;
}
tbody td {
  cursor: pointer;
  border-radius: 100%;
}
tbody td.selected {
  background: #8db3d3;
}
tbody td.selected:hover {
  background: #8db3d3;
}
tbody td:hover {
  background-color: #ffffff;
}
.calendar {
  background-color: #e6e6e6;
  border-radius: 5px;
  padding: 0.5em 0.2em;
  position: relative;
  top: 10px;
}
.calendar:before {
  content: '';
  width: 0;
  height: 0;
  border: solid transparent 8px;
  border-bottom: solid #e6e6e6 8px;
  position: absolute;
  bottom: 100%;
  left: 1em;
}
[v-cloak] {
  display: none;
}
</style>