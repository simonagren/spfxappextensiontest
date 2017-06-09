## SPFX Application Customizer
Just an example to call the Graph via the new GraphHttpClient (No ADAL) and then brand the header with the display name.
Used some of Mikael Svenson's (www.techmikael.com/) code to call the graph.
And used some sample code from https://github.com/SharePoint/sp-dev-fx-extensions

1. You need a developer tenant https://dev.office.com/devprogram
2. Create a modern teamsite/group via the SharePoint startpage.
3. Navigate to the document library.
4. Add following querystring:
?loadSPFX=true&debugManifestsFile=https://localhost:4321/temp/manifests.js&customActions={%226ed4a222-c0c8-441e-ae2e-d2240084deff%22:{%22location%22:%22ClientSideExtension.ApplicationCustomizer%22}} 

Full Example url:
https://tenantname.sharepoint.com/sites/TestGroup/Delade%20dokument/Forms/AllItems.aspx?loadSPFX=true&debugManifestsFile=https://localhost:4321/temp/manifests.js&customActions={%226ed4a222-c0c8-441e-ae2e-d2240084deff%22:{%22location%22:%22ClientSideExtension.ApplicationCustomizer%22}}

### Building the code

```bash
git clone the repo
npm i
npm i -g gulp
gulp
```

This package produces the following:

* lib/* - intermediate-stage commonjs build artifacts
* dist/* - the bundled script, along with other resources
* deploy/* - all resources which should be uploaded to a CDN.

### Build options

gulp clean - TODO
gulp test - TODO
gulp serve - TODO
gulp bundle - TODO
gulp package-solution - TODO
