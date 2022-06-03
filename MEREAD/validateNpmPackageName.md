# validate-npm-package-name

校验是否符合 npm 软件包名的工具函数

## npm 包名称规范

-   长度不为 0
-   不能以 `.` 、`_`开头
-   不能包含首尾空格
-   不包含大写字母
-   不能与 NodeJS 内置模块重名,且不能为保留字
-   不能包括 `~'!()*` 字符
-   长度上限为 214
-   需为 url 安全字符串

## 实现思路

1.  参数：字符串
2.  返回值：

    ```ts
    {
      validForNewPackages: boolean;
      validForOldPackages: boolean;
      warnings?: Array<string>;
      errors?: Array<string>;
    }
    ```

3.  逐次判断并收集错误/警告信息，并兼容带有命名空间的包名
4.  根据错误/警告信息数组判断名称是否有效，返回结果

## API

### 字符串正则相关

1. `String.prototype.match()`
2. `RegExp.prototype.test()`

### URL 相关

-   `encodeURIComponent()`
