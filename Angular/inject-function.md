# Angular Inject Function：你还在使用构造函数注入依赖吗

毫无疑问，依赖注入（DI）是 Angular 框架中很重要的一部分。简单来说，注入器（Injector）会维护一个关于如何创建依赖的列表，我们可以从注入器获取依赖关系。这些功能始终是借助类的构造函数来实现的。自从 Angular 14 开始，有一个强大的新方案可以替代基于构造函数的 DI，也就是本篇文章的主角 - Inject Function。

## 什么是 Inject Function

在讲 Inject Function 之前，先来回顾一下传统的基于构造函数的 DI 是怎样使用的。

在传统的用法中，Angular 中的组件、指令或者管道如果需要使用某个服务，必须通过构造函数参数注入才可以使用。

```typescript
@Injectable({
  providedIn: 'root',
})
export class DataService {
  constructor() {}
}

@Component({
...
})
export class AppComponent {
  constructor(private dataService: DataService) {}
}
```

如果这个服务的 `Token` 不是类而是 `InjectionToken`，则需要通过 `@Inject()` 参数装饰器使用：

```typescript
@Component({
...
})
export class AppComponent {
  constructor(@Inject(THEME_TOKEN) private themeService: ThemeService) { }
}
```

接下来看一下 Inject Function 的写法：

```ts

```

## 参考资料

- [Understanding dependency injection](https://angular.io/guide/dependency-injection)
- [Unleash the power of the inject function in Angular applications](https://medium.com/javascript-everyday/unleash-the-power-of-the-inject-function-in-angular-applications-8dc544f9edb8)
- [Angular v14 被低估的一个 DI 特性 inject](https://zhuanlan.zhihu.com/p/532236092)
