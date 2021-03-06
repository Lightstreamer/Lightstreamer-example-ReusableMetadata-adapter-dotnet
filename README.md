# Lightstreamer - Reusable Metadata Adapters - .NET Adapter

<!-- START DESCRIPTION lightstreamer-example-reusablemetadata-adapter-dotnet -->

<b>WARNING. This project is obsolete, the relevant code has been merged into this project [Lightstreamer .Net Remote Adapter SDK](https://github.com/Lightstreamer/Lightstreamer-lib-adapter-dotnet-remote#literalbasedprovider); which you need to refer to for an updated version of the LiteralBasedProvider Metadata Adapter.</b>

This project includes a simple full implementation of Remote Metadata Adapter in C#/.NET made available as sample for inspiration and/or extension.

## LiteralBasedProvider Metadata Adapter

The LiteralBasedProvider is a C#/.NET implementation of the *LiteralBasedProvider* Metadata Adapter in [Lightstreamer - Reusable Metadata Adapters - Java Adapters](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-java).
It extends the <i>MetadataProviderAdapter</i> class (which in turn implements the <i>IMetadataProvider</i> interface).
It is used in Lightstreamer examples and demos based on the [.NET Standard Adapter SDK](https://github.com/Lightstreamer/Lightstreamer-lib-adapter-dotnet-remote), in combination with suitable Data Adapters and Clients.


<!-- END DESCRIPTION lightstreamer-example-reusablemetadata-adapter-java -->
<br>

## Build

If you are testing your own modified version of the LiteralBasedProvider code, take care of changing the namespace name, or, at least, the class name.

To build your own version of the LiteralBasedProvider binaries, follow these steps:
* Download this project.
* Create a project for a library target and name it "DotNetGenericAdapters",
* Include in the project the sources `src`.
* Get the binaries files of the Lightstreamer .NET Standard Adapters Server library from NuGet [Lightstreamer.DotNetStandard.Adapters](https://www.nuget.org/packages/Lightstreamer.DotNetStandard.Adapters/), copy it into the `lib` directory and add it as a reference for the project; or more simply, use directly the "NuGet Package Manager" looking for 'Lightstreamer Adapters' and installing the *Lightstreamer.DotNetStandard.Adapters* package.
* Build Solution

### Deploy

To use the Metadata Adapter just built in some Remote Server, just include the `DotNetGenericAdapters.dll` library in addition to `DotNetStandardAdapter.dll`.


## See Also
<!-- START RELATED_ENTRIES -->

* [Lightstreamer .Net Remote Adapter SDK](https://github.com/Lightstreamer/Lightstreamer-lib-adapter-dotnet-remote)
* [Lightstreamer - Reusable Metadata Adapters - Java Adapter](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-java)
* [Lightstreamer - Reusable Metadata Adapters - Java Remote Adapter](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-java-remote)
* [Lightstreamer - Portfolio Demo - .NET Adapter](https://github.com/Lightstreamer/Lightstreamer-example-Portfolio-adapter-dotnet)
* [Lightstreamer - Stock-List Demo - .NET Adapter](https://github.com/Lightstreamer/Lightstreamer-example-Stocklist-adapter-dotnet)

<!-- END RELATED_ENTRIES -->

## Lightstreamer Compatibility Notes

* Compatible with Lightstreamer SDK for .NET Standard Adapters version 1.12.
* For instructions compatible with Lightstreamer SDK for .NET Adapters versions 1.10, please refer to [this tag](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-dotnet/releases/tag/for_1.10).
