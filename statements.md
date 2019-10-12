# Statements

## Function declaration statement

### Without arguments, Without return type

```
fn name() {

}
```

### Without arguments, With return type

```
fn name() => R {

}
```

### With arguments, Without return type

```
fn name(arg1: T1, arg2: T2, ..., argN: TN) {

}
```

### With arguments, With return type

```
fn name(arg1: T1, arg2: T2, ..., argN: TN) => R {

}
```

## Variable declaration statement

### Without type information, Without value

```
let name;
```

### Without type information, With value

```
let name = E;
```

### With type information, Without value

```
let name: T;
```

### With type information, With value

```
let name: T = E;
```
