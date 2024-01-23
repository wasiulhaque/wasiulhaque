```csharp
using System;

[AttributeUsage(AttributeTargets.Class)]
public class DataClassAttribute : Attribute
{
    public bool UnsafeHash { get; }
    public bool Frozen { get; }

    public DataClassAttribute(bool unsafeHash = false, bool frozen = false)
    {
        UnsafeHash = unsafeHash;
        Frozen = frozen;
    }
}

[DataClass(unsafeHash: true, frozen: true)]
class Bio
{
    public string Name { get; init; } = "Wasiul Haque";
    public string Designation { get; init; } = "Junior Software Engineer";
    public string Company { get; init; } = "Reve Systems";
    public string Base { get; init; } = "Dhaka, Bangladesh";
}

[DataClass(unsafeHash: true, frozen: true)]
class Stack
{
    public string[] Languages { get; init; } = { "C#", "JavaScript", "Python" };
    public string[] Frameworks { get; init; } = { "ASP.Net", "FastAPI", "ReactJS" };
    public string[] Databases { get; init; } = { "MySQL", "PostgreSQL", "Mongo" };
    public string[] Learning { get; init; } = { "Docker", "GraphQL", "Rust" };
}

[DataClass(unsafeHash: true, frozen: true)]
class Social
{
    public string Twitter { get; init; } = "WasiulHq";
    public string LinkedIn { get; init; } = "wasiul-haque";
}
