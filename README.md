# cuid2-issue

This is a sample app to show the following issue for @paralleldrive/cuid2.

https://github.com/paralleldrive/cuid2/issues/44

## Steps to recreate issue

```bash
npm run test
```

Output:

```
TypeError: Expected input type is Uint8Array (got object)

      2 | import { fetchCount } from './counterAPI';
      3 | import 'fast-text-encoding'
    > 4 | import { createId } from '@paralleldrive/cuid2'
```

## Steps to create this app

```bash
npx create-react-app cuid2-issue --template redux
npm add @paralleldrive/cuid2
npm add fast-text-encoding

# modified src/features/counter/counterSlice.js for the redux value to have createId() instead of an integer
```
