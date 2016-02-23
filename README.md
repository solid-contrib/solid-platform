# solid-platform
[![](https://img.shields.io/badge/project-Solid-7C4DFF.svg?style=flat-square)](https://github.com/solid/solid)

Servers, Tools and packages built on the
[Solid platform](https://github.com/solid/solid-spec).
(See also [solid-apps](https://github.com/solid/solid-apps) for a list of
end-user applications).

## Servers
Actively maintained, open source.

Name | LDP | Cors | WebID provider | WebID-TLS | WebID-RSA | WebID-Delegation | WAC   
-----|-----|------|----------------|-----------|-----------|------------------|----
[rww-play](https://github.com/read-write-web/rww-play)|Basic Containers, file storage, SEARCH|Proxy|Yes|Yes|No|N/A|Yes
[gold](https://github.com/linkeddata/gold)|Basic Containers, file storage|Proxy|Yes|Yes|Yes|Yes|Yes
[ldnode](https://github.com/linkeddata/ldnode)|In progress, file storage|N/A|No|Yes|No|No|Yes

##### [ldnode](https://github.com/linkeddata/ldnode)
Reference Solid platform server written in Node.js/Express.

##### [gold](https://github.com/linkeddata/gold)
Reference Solid platform server written in Go.
See [databox.me](https://databox.me/) for an example instance.
No longer under active development (the team is focusing on LDNode),
but is in bugfix/maintenance mode.

##### [rww-play](https://github.com/read-write-web/rww-play)
LDP-compliant Read-Write-Web server written in Scala/Play/akka.

## Incubator/Closed Source Servers
Actively maintained, closed source.

Name | LDP | Cors | WebID provider | WebID-TLS | WebID-RSA | WebID-Delegation | WAC   
-----|-----|------|----------------|-----------|-----------|------------------|----
[meccano](https://github.com/Qatar-Computing-Research-Institute/qcri-crosscloudP/tree/meccano)|Basic Containers (adaptor), SPARQL store|No|No|No|No|No|Partial

## Legacy Servers
No longer actively maintained.

##### [ldphp](https://github.com/linkeddata/ldphp)
LDP PHP server, implementing LDP Basic Containers and file serving.
Not implemented: WAC, WebID-RSA or WebID-Delegation.

## Libraries

### Node.js
* [node-webid](https://github.com/linkeddata/node-webid/) - library to manage
    [WebID](http://www.w3.org/2005/Incubator/webid/spec/identity/) identities
    and certificates.

* [rdflib.js](https://github.com/linkeddata/rdflib.js/) - RDF library for
    [Linked Data](http://www.w3.org/DesignIssues/LinkedData.html) applications.

* [solid.js](https://github.com/solid/solid.js) - library to interact with
    [Solid](https://github.com/solid/solid-spec)-compliant applications.
    Creates and manages LDP containers, provides WebID authentication, and more.
