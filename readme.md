# Packaging Helm Chart as a NuGet Package

This repository provides a template for packaging a Helm chart into a NuGet package.

## Folder Structure

Ensure your repository is structured as follows:

```plaintext
.
├── charts
│   └── your-chart
│       ├── Chart.yaml
│       ├── values.yaml
│       └── templates
│           └── ...
└── your-chart.nuspec
```


## Steps to Create NuGet Package

Follow these steps to create a NuGet package for your Helm chart:

1. **Install NuGet CLI**

   Ensure you have the NuGet CLI installed. If not, install it using the following command:

   ```bash
   sudo apt-get install -y nuget
   ```
Or download it from NuGet CLI.

2. **Create the NuGet Package**

   Navigate to the directory containing your .nuspec file and run the following command:
   ```bash
   nuget pack your-chart.nuspec
   ```

3. **Publish the NuGet Package**

   To publish your NuGet package to NuGet.org or any other NuGet server, use the following   command:
   ```bash
   nuget push YourHelmChart.1.0.0.nupkg -Source https://api.nuget.org/v3/index.json -ApiKey YOUR_NUGET_API_KEY
   ```
Replace YOUR_NUGET_API_KEY with your actual NuGet API key.
