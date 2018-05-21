<a href="http://jsdaddy.io/img/logo.png">
  <h1 align="center">NGX Loader INDICATOR</h1>
</a>

<p align="center">
  NGX LOADER INDICATOR is the best directive without wrapping your element to additional component
</p>

## Installing

```bash
$ npm install --save ngx-loader-indicator
```

## Quickstart

Import **ngx-loader-indicator** module in Angular app.

```typescript
import {NgxLoaderIndicatorModule} from 'ngx-loader-indicator'

(...)

@NgModule({
  (...)
  imports: [
    NgxLoaderIndicatorModule.forRoot(options)
  ]
  (...)
})
```

### Usage

```html
<div loader [show]="isLoading">Content</div> 
```

#### Examples

```html
<form (ngSubmit)="save(form.value)" [formGroup]="form" loader [show]="isLoading">
  <h2>Login</h2>
  <input matInput type="email" placeholder="Email" #email formControlName="email">
  <input matInput type="password" placeholder="Password" #name formControlName="password">
  <button mat-button [disabled]="form.invalid">Login</button>
</form>
```

## ngx-loader-indicator Options
You can define your custom options


### custom img (string) and colors
```typescript
  {
    img: string,
    imgStyles: {
      width: string, // '30px'
      background: string, // 'yellow' or rgb(255, 255, 0)
    }
  }
```

### custom wrapper layout colors
```typescript
  {
    loaderStyles: {
      background: string,
    },
  }
```

### animations options for image rotation
```typescript
    rotate: {
      delay?: number;
      direction?: 'normal' | 'reverse' | 'alternate' | 'alternate-reverse';
      duration: number
      easing?: string;
      endDelay?: number;
      fill?: 'none' | 'forwards' | 'backwards' | 'both' | 'auto';
      id?: string;
      iterationStart?: number;
      iterations?: number;
    },
```


### Usage
```typescript
import {NgxLoaderIndicatorModule} from 'ngx-loader-indicator'

(...)

@NgModule({
  (...)
  imports: [
    NgxLoaderIndicatorModule.forRoot({
      img: 'https://avatars2.githubusercontent.com/u/32452610?s=200&v=4',
      loaderStyles: {
        background: 'rgba(255, 255, 255, 0.8)',
      },
      imgStyles: {
        width: '100px',
        background: 'yellow',
      },
      rotate: {
        duration: 5000
      },
    }),
  ]
  (...)
})
```
