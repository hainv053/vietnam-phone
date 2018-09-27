# vietnam-phone

Detect vietnam phonenumber, support new province code.

## Installation

```bash
npm install vietnam-phone --save
```
or
```bash
yarn add vietnam-phone
```

## API
- `detectPhoneNumber(phone_number: string)`: Response
    + `phone_number`: String
    + `old_number`: String, Old phone number using old province code
    + `new_number`: String, New phone number using new province code
    + `is_change`: Boolean, Status check phone number old phone or new phone
    + `vendor`: String, {`VIETTEL`, `VINAPHONE`, `MOBIFONE`, `VIETNAMOBILE`,`BEELINE`}

## Usage

```ts
import { detectPhoneNumber } from 'vietnam-phone';

console.log(detectPhoneNumber('01693234345'));

# Response
# {phone_number: "01693234345", old_number: "01693234345", new_number: "0393234345", is_change: true, vendor: "VIETTEL"}

console.log(detectPhoneNumber('0393234345'));

# Response
# {phone_number: "0393234345", old_number: "01693234345", new_number: "0393234345", is_change: true, vendor: "VIETTEL"}

```