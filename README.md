# SBOM
I want to learn about Graph Databases by making a Software Bill of Materials

yay souptime.
What is a Software Bill of Materials? An SBOM shows the components of software. It is useful in the enterprise (or at home) for created projects, open-source programs, and commercial packages. A SBOM would be useful for tracking which programs are being used in the org. It should contain the versions of programs and packages being used (to see if they are up-to-date). Ideally, it would help with licensing/license/certificate management. It should help with vulnerability tracking and mitigation. 

a graph database would be selected because it contains a hot data science buzzword; but also because a graph database is optimised for searching and finding relationships. If a library is found to have a security problem (ex. embedded passwords) then the graph database should be able to efficiently discover where that package exists throughout the database. A traditional database would be able to achieve this, but I would expect difficulties. The library would not necessarily be in same place, depending on the context of the usage. 
An example is that my program may use Netmiko, which has a version, size, hash, etc. Netmiko uses paramiko, which uses other libraries. if paramiko used pandas for something, and my program also used pandas, but they used different versions, they would be a different levels and may be difficult to find in SQL. Its also possible that my program does an update to a new version. Could the database flag that now paramiko (or other package) is now using an older version of pandas?

What are existing open source graph databases? 
------------------------------------------------
neo4j is one of the popular ones. I will probably give this one a try first. Free is good for trying and learning things.
  https://neo4j.com/developer/graph-visualization/
  
ArangoDB is built for graphs and JSON
    https://www.arangodb.com/
GraphDB may have functionality for both noSQL and SQL
    https://graphdb.ontotext.com/

Are there existing SBOMs?
-------------------------------------------
Yes. there are many SBOM products, and some open source ones. I couldn't find anything that was based on a graph database. A graph database is optimised for relationships, which is one of things we want for a SBOM.
https://devblogs.microsoft.com/engineering-at-microsoft/microsoft-open-sources-salus-software-bill-of-materials-sbom-generation-tool/
Here is the link for the microsoft tool - https://github.com/microsoft/sbom-tool
