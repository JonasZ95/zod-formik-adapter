# zod-formik-adapter

This library adapts a [zod](https://www.npmjs.com/package/zod) schema to work as a `validationSchema` prop on [Formik](https://www.npmjs.com/package/formik)

**IMPORTANT: Currently, this library does not work with zod union. See more [here](https://github.com/robertLichtnow/zod-formik-adapter/issues/2).**

## Install

```sh
# npm
$ npm install zod-formik-adapter

# yarn
$ yarn add zod-formik-adapter
```

## Usage

```TSX
import { z } from 'zod';
import { Formik } from 'formik';
import { toFormikValidationSchema } from 'zod-formik-adapter';

const Schema = z.object({
  name: z.string(),
  age: z.number(),
});

const Component = () => (
  <Formik
    validationSchema={toFormikValidationSchema(Schema)}
  >
    {...}
  </Formik>
);
```
