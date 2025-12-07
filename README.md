# Olbrasoft.Data.Paging.X.PagedList

[![Build & Publish](https://github.com/Olbrasoft/Data.Paging.X.PagedList/actions/workflows/publish-nuget.yml/badge.svg)](https://github.com/Olbrasoft/Data.Paging.X.PagedList/actions/workflows/publish-nuget.yml)
[![NuGet](https://img.shields.io/nuget/v/Olbrasoft.Data.Paging.X.PagedList.svg)](https://www.nuget.org/packages/Olbrasoft.Data.Paging.X.PagedList/)
[![NuGet Downloads](https://img.shields.io/nuget/dt/Olbrasoft.Data.Paging.X.PagedList.svg)](https://www.nuget.org/packages/Olbrasoft.Data.Paging.X.PagedList/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![.NET](https://img.shields.io/badge/.NET-8.0%20%7C%209.0%20%7C%2010.0-blue)](https://dotnet.microsoft.com/)

Extension methods for converting `Olbrasoft.Data.Paging.IBasicPagedResult` to [X.PagedList](https://github.com/dncuug/X.PagedList).

## Installation

```bash
dotnet add package Olbrasoft.Data.Paging.X.PagedList
```

## Features

- **AsPagedList()** - Convert `IBasicPagedResult<T>` to `IPagedList<T>`
- Seamless integration between Olbrasoft.Data.Paging and X.PagedList
- Supports both synchronous and asynchronous scenarios

## Usage

```csharp
using Olbrasoft.Data.Paging.X.PagedList;

// Convert IBasicPagedResult to IPagedList
IBasicPagedResult<User> pagedResult = await userService.GetUsersAsync(page, pageSize);
IPagedList<User> pagedList = pagedResult.AsPagedList();

// Use in MVC views with X.PagedList.Mvc.Core
<pager list="@pagedList" options="@PagedListRenderOptions.Bootstrap4" />
```

## Related Packages

- [Olbrasoft.Data.Paging](https://www.nuget.org/packages/Olbrasoft.Data.Paging/) - Core paging abstractions
- [Olbrasoft.Data.Paging.X.PagedList.AspNetCore.Mvc](https://www.nuget.org/packages/Olbrasoft.Data.Paging.X.PagedList.AspNetCore.Mvc/) - TagHelper for ASP.NET Core MVC

## Target Frameworks

- .NET Standard 2.0, 2.1
- .NET 8.0, 9.0, 10.0

## License

MIT License - **Copyright © 2019-2025 Olbrasoft**

---

![Olbrasoft X.PagedList](./olbrasoft-x-paged-list.png)
