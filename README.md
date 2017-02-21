# Lightstreamer - Reusable Metadata Adapters - .NET Adapter

<!-- START DESCRIPTION lightstreamer-example-reusablemetadata-adapter-dotnet -->

This project includes a simple full implementation of Remote Metadata Adapter in C#/.NET made available as sample for inspiration and/or extension.

## LiteralBasedProvider Metadata Adapter

The LiteralBasedProvider is a C#/.NET implementation of the *LiteralBasedProvider* Metadata Adapter in [Lightstreamer - Reusable Metadata Adapters - Java Adapters](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-java).
It extends the [MetadataProviderAdapter](http://www.lightstreamer.com/docs/adapter_dotnet_api/Lightstreamer_Interfaces_Metadata_MetadataProviderAdapter.html) class (which in turn implements the [IMetadataProvider](http://www.lightstreamer.com/docs/adapter_dotnet_api/Lightstreamer_Interfaces_Metadata_IMetadataProvider.html) interface).
It is used in Lightstreamer examples and demos based on the .NET Adapter SDK, in combination with suitable Data Adapters and Clients.
Its binaries are included in the .NET Adapter SDK library.

<!-- END DESCRIPTION lightstreamer-example-reusablemetadata-adapter-java -->
<br>
<br>

## Build

Note that `DotNetAdapter_N2.dll`, provided within the .NET Adapter SDK, already includes the binaries for Lightstreamer.Adapters.Metadata.LiteralBasedProvider; we can ignore that for a moment.
If you are testing your own modified version of the LiteralBasedProvider code, take care of changing the namespace name, or, at least, the class name.

To build your own version of the LiteralBasedProvider binaries, follow these steps:
* Download this project.
* Create a project for a library target and name it "DotNetGenericAdapters_N2",
* Include in the project the sources `src`.
* Get the Lightstreamer .NET Adapter SDK library `DotNetAdapter_N2.dll` file from the `DOCS-SDKs/sdk_adapter_dotnet/lib` folder of the [latest Lightstreamer distribution](http://download.lightstreamer.com/#current), and copy them into the `lib` directory.
* Include in the project the references to `DotNetAdapter_N2.dll` from the `lib` folder.
* Build Solution

### Deploy

To use the Metadata Adapter just built in some Remote Server, just include the `DotNetGenericAdapters_N2.dll` library in addition to `DotNetAdapter_N2.dll`.
As said, the binaries for Lightstreamer.Adapters.Metadata.LiteralBasedProvider are already included in `DotNetAdapter_N2.dll`, which is part of the .NET Adapter SDK; hence this step is not needed for the LiteralBasedProvider.

The LiteralBasedProvider can be configured through suitable initialization parameters. See the [class documentation](http://www.lightstreamer.com/docs/adapter_dotnet_api/Lightstreamer_Adapters_Metadata_LiteralBasedProvider.html) for details.
For instance, you can run the supplied Remote .NET Adapter Server to host the LiteralBasedProvider through a command like the following:<br/>
`start "LiteralBasedProvider" /MIN DotNetServer_N2 Lightstreamer.Adapters.Metadata.LiteralBasedProvider /host localhost /rrport 6663 max_bandwidth=40 max_frequency=3 buffer_size=30`<br/>

## See Also
<!-- START RELATED_ENTRIES -->

* [Lightstreamer - Reusable Metadata Adapters - Java Adapter](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-java)
* [Lightstreamer - Reusable Metadata Adapters - Java Remote Adapter](https://github.com/Lightstreamer/Lightstreamer-example-ReusableMetadata-adapter-java-remote)
* [Lightstreamer - Portfolio Demo - .NET Adapter](https://github.com/Lightstreamer/Lightstreamer-example-Portfolio-adapter-dotnet)
* [Lightstreamer - Stock-List Demo - .NET Adapter](https://github.com/Lightstreamer/Lightstreamer-example-Stocklist-adapter-dotnet)

<!-- END RELATED_ENTRIES -->

## Lightstreamer Compatibility Notes

* Compatible with Lightstreamer SDK for .NET Adapters versions 1.7 to 1.9.
