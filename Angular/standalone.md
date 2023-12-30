# Angular 独立组件：你还在使用 NgModule 吗

自从 v14 开始，Angular 就引入了独立组件（Standalone components）的功能，直到最近发布的 v17 版本，独立组件成了使用 Angular cli 创建项目时的默认方式。

那么独立组件到底是什么，相比使用 NgModule，又有什么优缺点呢？

## 什么是独立组件

简单来说，独立组件（Standalone components）允许我们在不使用 `NgModule` 的情况下构建 Angular 应用程序。它们不需要依赖于任何特定模块，可以在应用程序的任何部分使用。

在当前版本，Angular 团队始终建议使用独立组件，当然，并不是只能使用独立组件，我们也可以混合 `NgModule` 使用。个人认为独立组件并不是用来取代 `NgModule`，而是提供了一种新的可选方式。

通过在组件、指令或者管道的元数据中添加 `standalone: true`，来指明该组件是一个独立组件。独立组件直接指定它们的依赖项，而不是把相关代码组织到 `NgModule` 中。

## 创建独立组件

先来看一个简单的例子：

```ts
import { Component } from '@angular/core';
import { CommonModule } from '@angular/common';
import { RouterOutlet } from '@angular/router';

@Component({
  selector: 'app-root',
  standalone: true,
  imports: [CommonModule, RouterOutlet],
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  title = 'ng-17-demo';
}
```
