# Universal Age Calculator

[![npm version](https://badge.fury.io/js/%40awaisbaig%2Fage-calculator.svg)](https://badge.fury.io/js/%40awaisbaig%2Fage-calculator)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A modern, **framework-agnostic** age calculator library for JavaScript and TypeScript. Works seamlessly with **React**, **Angular**, **Vue**, **Svelte**, and vanilla JavaScript. This is an enhanced version of the original [@dipaktelangre/age-calculator](https://www.npmjs.com/package/@dipaktelangre/age-calculator) package, rebuilt from the ground up with modern ESM support.

## Features

🌐 **Framework Agnostic** - Works with React, Angular, Vue, Svelte, and vanilla JS  
🎯 **TypeScript First** - Full TypeScript support with type definitions  
📦 **Tree-shakeable** - Optimized bundle size with ES modules  
🧪 **Well Tested** - Comprehensive unit tests with Vitest  
🚀 **Easy to Use** - Simple and intuitive static API  
⚡ **Zero Dependencies** - Lightweight with no external dependencies  
📱 **Modern Build** - ESM and CommonJS support via tsup  

## Installation

```bash
npm install @awaisbaig/age-calculator
```

## Quick Start

### Vanilla JavaScript / TypeScript

```typescript
import { AgeCalculator } from '@awaisbaig/age-calculator';

// Get age breakdown
const age = AgeCalculator.getAge(new Date('1990-01-01'));
console.log(age); // { years: 34, months: 6, days: 3 }

// Get age in specific unit
const years = AgeCalculator.getAgeIn(new Date('1990-01-01'), 'years');
console.log(years); // 34

// Check if adult
const isAdult = AgeCalculator.isAdult(new Date('1990-01-01'));
console.log(isAdult); // true
```
## API Reference

### `AgeCalculator.getAge(dateOfBirth: Date, currentDate?: Date): AgeResult`

Calculate age breakdown in years, months, and days.

```typescript
const age = AgeCalculator.getAge(new Date('1990-01-01'));
// Returns: { years: 34, months: 6, days: 3 }
```

**Parameters:**
- `dateOfBirth` - Date of birth
- `currentDate` - Optional. Current date (defaults to today)

**Returns:** `AgeResult` object with `years`, `months`, and `days`

---

### `AgeCalculator.getAgeIn(dateOfBirth: Date, unit: AgeUnit, currentDate?: Date): number`

Calculate age in a specific unit.

```typescript
const years = AgeCalculator.getAgeIn(new Date('1990-01-01'), 'years');
// Returns: 34

const months = AgeCalculator.getAgeIn(new Date('1990-01-01'), 'months');
// Returns: 414

const weeks = AgeCalculator.getAgeIn(new Date('1990-01-01'), 'weeks');
// Returns: 1800

const days = AgeCalculator.getAgeIn(new Date('1990-01-01'), 'days');
// Returns: 12600
```

**Parameters:**
- `dateOfBirth` - Date of birth
- `unit` - Unit to calculate: `'years'` | `'months'` | `'weeks'` | `'days'` | `'hours'` | `'minutes'` | `'seconds'`
- `currentDate` - Optional. Current date (defaults to today)

**Returns:** Age as a number in the specified unit

---

### `AgeCalculator.isAdult(dateOfBirth: Date, currentDate?: Date): boolean`

Check if a person is an adult (18 years or older).

```typescript
const adult = AgeCalculator.isAdult(new Date('2000-01-01'));
// Returns: true
```

---

### `AgeCalculator.getNextBirthday(dateOfBirth: Date, currentDate?: Date): Date`

Get the date of the next birthday.

```typescript
const nextBirthday = AgeCalculator.getNextBirthday(new Date('1990-12-25'));
// Returns: Date object for next December 25th
```

---

### `AgeCalculator.getDaysUntilNextBirthday(dateOfBirth: Date, currentDate?: Date): number`

Get the number of days until the next birthday.

```typescript
const daysUntil = AgeCalculator.getDaysUntilNextBirthday(new Date('1990-12-25'));
// Returns: number of days
```

---

### `AgeCalculator.getZodiacSign(dateOfBirth: Date): string`

Get the zodiac sign based on date of birth.

```typescript
const sign = AgeCalculator.getZodiacSign(new Date('1990-04-15'));
// Returns: 'Aries'
```

## Development

### Build the Library

```bash
npm run build
```

### Run Tests

```bash
npm test
```

### Watch Mode

```bash
npm run test:watch
```

## TypeScript Support

Full TypeScript support with exported types:

```typescript
import { AgeCalculator, AgeResult, AgeUnit } from '@awaisbaig/age-calculator';

const age: AgeResult = AgeCalculator.getAge(new Date('1990-01-01'));
const unit: AgeUnit = 'years';
```

## Bundle Size

- **ESM**: ~2KB (minified + gzipped)
- **CJS**: ~2KB (minified + gzipped)
- **Zero dependencies**

## Browser Support

Works in all modern browsers and Node.js 16+:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Node.js 16+

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT © Awais Baig

## Credits

Inspired by the original [@dipaktelangre/age-calculator](https://github.com/dipaktelangre/age-calculator) package by Dipak Telangre.

## Changelog

### 1.0.0
- Initial release
- Framework-agnostic design
- Full TypeScript support
- ESM and CommonJS support
- Enhanced API with additional methods
- Comprehensive test coverage with Vitest
- Zero dependencies
- Modern build system with tsup
