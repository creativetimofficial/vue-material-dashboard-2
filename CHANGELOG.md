# Change Log

## [3.0.0] 2022-06-14

- Rename components name prefix from Vmd to Material

## [2.0.0] 2022-04-20

### Bug fixing

### Major style changes

- `VmdAvatar`'s `img` prop is set to `required`.
- Update `VmdButton` default `color` to “success”.
- Update `checked` prop of `VmdCheckbox` from “string” to “boolean”.
- `id` of `VmdInput` is set to required.
- `VmdPagination`'s default `color` set to “success” and default `size` to “md”.
- Update `VmdPogress` default color to “success” and `percentage`'s type to Number. And `percentage` is set to required.
- `VmdRadio`'s `id`, and `name` props set to required and `checked` prop type changed to Boolean.
- The following changes were made to `VmdSnackbar`.
  - `title` prop set to required.
  - Deleted `iconColor` and `iconName` props.
  - Added `icon` prop type of object with `component`, and `color` keys.
- `VmdSwitch`'s `name`, `id` props set to required. `checked` prop data type changed from String to Boolean. And removed `inputClass` prop and instead any class added to the component will directly be added to input tag.
- `VmdTextArea`'s `id` set to required.
- Renamed and refactored `MiniCards` to `MiniStatisticsCard` component and added the following props:

  - Required `title` prop of type Object with the following keys:
    - `text` of type String.
    - `value` of type Number, and String.
  - `detail` of type String.
  - Required `icon` prop type of Object with the following keys:
    - `name`, `color`, and `background` of type String.

- Added `ChartHolderCard` component with default slot for `chart` component and the : `title`, `subtitle`, `update`, and `color` props of type String.
  - Added `ReportsBarChart` component with the following props and keys:
    - `id` of type String.
    - `height` of type Number, and String.
    - Required `chart` of type Object with required value and the following keys:
      - `labels` of type Array.
      - `datasets` of type Object with the following keys:
        - `label` of type String.
        - `data` of type Array.
  - Added `ReportsLineChart` component with the following props and keys:
    - `id` of type String.
    - `height` of type Number, and String.
    - Required `chart` of type Object with required value and the following keys:
      - `labels` of type Array.
      - `datasets` of type Object with the following keys:
        - `label` of type String.
        - `data` of type Array.
- Renamed `ProjectsCard` component to `ProjectCard` and restructured component with the following props:
  - `title` and `description` of type String.
  - `headers` of type Array.
  - Required `projects` of type Array with the following keys:
    - `logo`, `title`, and `budget` of type String.
    - `members` of type Array.
    - `progress` of type Object with `percentage`, and `color` keys.
- Added `TimelineList` component with a “default slot” and the following props:
  - `title`, and `description` of type String.
  - `darkMode` of type Boolean.
- Added `TimelineItem` component with the following props:
  - `color`, `icon`, `title`, `dateTime`, and `description` of type String.
  - `icon` of type object with the following keys:
    - `component` and `class` of type String.
- MasterCard `props` refactored to a single `card` prop `Object` with the following keys:
  - `number` accepts a `String` with the default value of `7852 4594 1122 4562`.
  - `holderText` accepts a `String` with the default value of `Card Holder`.
  - `holderName` accepts a `String` with the default value of `Jack Peterson`.
  - `expiryText` accepts a `String` with the default value of `Expirs`.
  - `expiryDate` accepts a `String` with the default value of `11/22`.
  - `background` accepts a `String` with the default value of `dark`.
- Refactored `DefaultInfoCard` component with the following props:
  - Required `icon` of type String and Object with the following keys:
    - `component`, and `background` of type String.
  - `title`, and `description` of type String.
  - `value` of type String and Number.
- Added `ProfileInfoCard` component with the following props:
  - `title`, and `description` of type String
  - `Info` of type Object with the following keys:
    - `fullName`, `mobile`, `email`, and `location` of type String.
  - `social` of type Array with the following acceptable keys:
    - `link`, and `icon` of type String.
  - `action` of type Object with the following keys:
    - `route`, and `tooltip` of type String.

Added `DefaultProjectCard` component with the following props:

- `image`, `label`, `title`, and `description` of type String.
- `action` of type Object with the following keys:
  - `route`, `color`, and `label` of type String.
- `authors` of type array with the following acceptable keys:
  - `image`, and `name` of type String.

### Deleted components

```
ChartBars.vue
ChartLine.vue
ChartLineTasks.vue
OrdersCard.vue
```

### Added components

```
ChartHolderCard
ReportsBarChart
ReportsLineChart
TimelineList
TimelineItem
ProfileInfoCard
DefaultProjectCard
```

### Deleted dependencies

### Added dependencies

### Updated dependencies

"vue-router" "4.0.0-0" -> "4.0.14"

### Warning

## [1.0.0] 2022-03-04

### Original Release
