# ng2-simple-dropdown
Angular2 Dropdown Component with *NO DEPENDENCYS*

***ng2-simple-dropdown*** is a table grid component for Angular2/4.

## Demo

Try it out: [http://ng2-simple-dropdown.nicolaszick.com](http://ng2-simple-dropdown.nicolaszick.com)

## Data

`[items]` can be an Object like the following:

```js
this.savedFilter = [
      {
        name: 'Profile1', 
        any: {}
      }
]
```

`[defaultValue]` can be a String like the following:

```js
this.defaultSelectTextProfile = "Please Select";
```

`[isEditable]` can be a boolean and defined if dropdown values can be changed


## Installation

Install ng2-simple-dropdown via `npm`

````shell
npm install ng2-simple-dropdown --save
````

## Integration

```ts
// app.module.ts
import { SimpleDropdownModule } from 'ng2-simple-dropdown';

@NgModule({
  ...
  imports: [ SimpleDropdownModule ]
  ...
})
export class AppModule { }

// app.component.html
<ng2-simple-dropdown [items]="items" [(ngModel)]="selectedItem" [defaultValue]="defaultText"></ng2-simple-dropdown>

// app.component.ts
import { Item } from 'ng2-simple-dropdown';

// ...

export class AppComponent {
  savedFilter: Item[] = [];
  selectedFilter: Item;
  defaultSelectTextProfile = 'Profiles';

  constructor() {
    const data = { };
    this.savedFilter = [
      new Item('Profile1'),
      new Item('Profile2'),
      new Item('Profile3', data),
      new Item('Profile4', data),
      new Item('Profile5', data),
      new Item('Profile6', data),
      new Item('Profile7', data),
      new Item('Profile8', data),
      new Item('Profile9', data),
      new Item('Profile10', data),
    ];
  }
}

```

## Run Included Demo

```shell
git clone https://github.com/fbele/ng2-simple-dropdown.git --depth 1
cd ng2-simple-dropdown
npm install
npm start
```

## AoT Library Build

```shell
npm run build:lib
```

## Licence

This project is licensed under the MIT license. See the [LICENSE](LICENSE) file for more info.
