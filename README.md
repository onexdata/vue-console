# vue-console
Original idea taken from console.js 1.2.2 (before it was ported to React and became complex)
Apache 2.0 License.

## Usage:

### In your app:
  import console from 'vue-console'
  Vue.use(console)

### Custom settings
```<v-console settings="yourSettingsHere" />```

### On any of your existing vue components
```
  commands: {
    support () {
      // Do stuff here to initially setup your command
      return {
        // Guide is what shows up in the help system
        guide: 'Contact a client specialist',
        // command is what gets executed when they type the command
        command () {
          // return is what is finally sent back to the console as output
          return 'Contacting a client solutions specialist, hold on...'
        }
      }
    },
    reboot () {
      return {
        guide: 'Restarts the program',
        command () {
          setTimeout(function () { location.reload() }, 1000)
          return '<span style="color: red">Rebooting...</span>'
        }
      }
    }
  }
```
