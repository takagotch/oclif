### oclif
---
https://github.com/oclif/oclif

```
npx oclif single mynewcli
./bin/run
npx oclif multi mynewcli
./bin/run --version
./bin/run --help
mynewcli [COMMAND]
./bin/run hello
```

```js
import {Command} from '@oclif/command'
export class GoodbyCommand extends Command {
  async run() {
    console.log('goodbye, world!')
  }
}

import Command, {flags} from '@oclif/command'

export class MyCommand extends Command {
  static description = `description of my command
    can be multiline
    `
    
  static hidden = false
  
  static usage = 'mycommand --myflag'
  
  static examples = [
    '$ mycommand --force',
    '$ mycommand --help',
  ]
  
  static strict = false
  
  async run() {
    this.warn('uh oh!')
    
    this.error('uh oh!!!')
    
    this.exit(1)
  }
}

this.log('hello')
this.warn('uh oh!')
this.warn(new Error('uh oh!'))

import {CLIError} from '@oclif/errors'
throw new CLIError('my friendly error')

this.exit()
this.exit(1)
```
  
```
```
