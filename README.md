# Be.Vlaanderen.Basisregisters.AspNetCore.Mvc.Middleware.DefaultResponseCompressionQuality [![Build Status](https://github.com/Informatievlaanderen/default-response-compression-quality-middleware/workflows/CI/badge.svg)](https://github.com/Informatievlaanderen/default-response-compression-quality-middleware/actions)

ASP.NET Core MVC Middleware to define default compression quality priorities.

## Usage

```csharp
public void Configure(IApplicationBuilder app, ...)
{
    app
        ...
        .UseMiddleware<DefaultResponseCompressionQualityMiddleware>(new Dictionary<string, double>
        {
            { "br", 1.0 },
            { "gzip", 0.9 }
        })
        ...
        .UseResponseCompression()
        ...
}
