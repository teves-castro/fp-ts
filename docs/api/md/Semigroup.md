MODULE [Semigroup](https://github.com/gcanti/fp-ts/blob/master/src/Semigroup.ts)

# Semigroup

_type class_

```ts
interface Semigroup<A> {
  concat: (x: A, y: A) => A
}
```

# semigroupAll

_instance_

```ts
Semigroup<boolean>
```

Boolean semigroup under conjunction

# semigroupAny

_instance_

```ts
Semigroup<boolean>
```

Boolean semigroup under disjunction

# semigroupProduct

_instance_

```ts
Semigroup<number>
```

Number Semigroup under multiplication

# semigroupString

_instance_

```ts
Semigroup<string>
```

# semigroupSum

_instance_

```ts
Semigroup<number>
```

Number Semigroup under addition

# semigroupVoid

_instance_

```ts
Semigroup<void>
```

# fold

_function_

```ts
<A>(S: Semigroup<A>) => (a: A) => (as: Array<A>): A
```

# getArraySemigroup

_function_

```ts
<A = never>(): Semigroup<Array<A>>
```

Semigroup under array concatenation

# getDualSemigroup

_function_

```ts
<A>(S: Semigroup<A>): Semigroup<A>
```

# getFirstSemigroup

_function_

```ts
<A = never>(): Semigroup<A>
```

# getFunctionSemigroup

_function_

```ts
<S>(S: Semigroup<S>) => <A = never>(): Semigroup<(a: A) => S>
```

# getJoinSemigroup

_function_

```ts
<A>(O: Ord<A>): Semigroup<A>
```

# getLastSemigroup

_function_

```ts
<A = never>(): Semigroup<A>
```

# getMeetSemigroup

_function_

```ts
<A>(O: Ord<A>): Semigroup<A>
```

# getProductSemigroup

_function_

```ts
<A, B>(SA: Semigroup<A>, SB: Semigroup<B>): Semigroup<[A, B]>
```

# getRecordSemigroup

_function_

```ts
<O extends { [key: string]: any }>(
  semigroups: { [K in keyof O]: Semigroup<O[K]> }
): Semigroup<O>
```
