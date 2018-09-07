# Nosnitor.TestFramework.AssemblyValidation

The Nosnitor.TestFramework.AssemblyValidation project provides a common interface to perform validation of Nosnitor .NET assemblies.

## Using AssemblyValidation

### Adding AssemblyValidation to your project

AssemblyValidation is available as a NuGet package at the following location:

[https://www.nuget.org/packages/Nosnitor.TestFramework.AssemblyValidation](https://www.nuget.org/packages/Nosnitor.TestFramework.AssemblyValidation)

### Create the assembly manifest for assemblies in your solution

The assembly manifest defines the expected values for attributes and properties validated by AssemblyValidation. The filename should be defined in the following format:

    {AssemblyName}.assembly_manifest.json

#### Example assembly_manifest.json

	{
	  "Assembly": "Nosnitor.TestFramework.AssemblyValidation.Core.dll",
	  "Title": "AssemblyValidation Core Library",
	  "Copyright": "Copyright © 2017-2018 Nosnitor Corporation",
	  "Product": "Nosnitor TestFramework",
	  "FileVersion": "1.0.0.0",
	  "InformationalVersion": "1.0.0-dev+jsblo.20180906.205820"
	}

The assembly manifest should be included with test assemblies for test execution.

### Execute the AssemblyValidation testing

Using the MSTest v2 test adapter, include the Nosnitor.TestFramework.AssemblyValidation.Tests assembly in your test execution pipeline.