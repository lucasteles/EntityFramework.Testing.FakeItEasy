# EntityFramework.Testing.FakeItEasy
<p align="center">
    <a href="https://ci.appveyor.com/project/mgibas/entityframework-testing-fakeiteasy/branch/master">
        <img src="https://ci.appveyor.com/api/projects/status/github/mgibas/entityframework.testing.fakeiteasy?branch=master&svg=true"></img>
    </a>
    <a href="https://www.gitcheese.com/app/#/projects/b6a20f9c-68b0-4c50-8fc2-e8c33e0baa51/pledges/create">
        <img src="https://api.gitcheese.com/v1/projects/b6a20f9c-68b0-4c50-8fc2-e8c33e0baa51/badges"></img>
    </a>
</p>

===

Simple EntityFramework FakeItEasy utility class - fell free and contribute!

Getting Started:

- Creating fake DbSet<T>:
```csharp
var fakeDbSet = Aef.FakeDbSet(new List<Model>{...});
A.CallTo(() => context.Models).Returns(fakeDbSet);
```

```csharp
var fakeDbSet =  Aef.FakeDbSet<Model>(55); //55 Model fakes created by FakeItEasy
A.CallTo(() => context.Models).Returns(fakeDbSet);
```

```csharp
var fakeDbSet = Aef.FakeDbSet<Model>(); //Empty collection
A.CallTo(() => context.Models).Returns(fakeDbSet);
```
