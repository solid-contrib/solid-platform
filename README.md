# solid-platform
[![](https://img.shields.io/badge/project-Solid-7C4DFF.svg?style=flat-square)](https://github.com/solid/solid)

Servers, tools and packages built on the
[Solid platform](https://github.com/solid/solid-spec).
(Also see lists of [end-user applications](https://github.com/solid/solid-apps) and [running implementations of Solid-compatible servers](https://github.com/solid/node-solid-server/wiki/Running-Test-Implementations-of-Solid-compatible-servers)).

## Servers
_(Note -- you will need to scroll the table to see all columns!)_

Name | Development Status | Project Type | [LDP](https://www.w3.org/TR/ldp/) | [CORS](https://github.com/solid/solid-spec/blob/master/recommendations-server.md) | [WebID](https://github.com/solid/solid-spec/blob/master/solid-webid-profiles.md) IdP | [WebID-TLS](https://github.com/solid/solid-spec/blob/master/authn-webid-tls.md) | [WebID-OIDC](https://github.com/solid/webid-oidc-spec) | [WebID-RSA](https://github.com/solid/solid/blob/master/proposals/auth-webid-rsa.md) | WebID-TLS + Delegation | [WAC](https://github.com/solid/web-access-control-spec) | [WSS](https://github.com/solid/solid-spec/blob/master/api-websockets.md) | 
-----|-----|-----|-----|:----:|:--------------:|:---------:|:----------:|:---------:|:----------------:|:---:|:---:|
[gold](https://github.com/linkeddata/gold) | Bugfix | Open Source | Basic Containers, file storage | Proxy | Yes | Yes | No | Yes | Yes | Yes | Yes | 
[ldphp](https://github.com/linkeddata/ldphp) | Inactive | Open Source | Basic Containers, file storage | ? | ? | ? | No | No | No | No | ? | 
[node-solid-server](https://github.com/solid/node-solid-server/) | Active | Open Source | Basic Containers, file storage | Proxy | Yes | Yes | Yes | No | In Progress | Yes | Yes | 
[OpenLink Virtuoso](http://virtuoso.openlinksw.com/) _(Enterprise Edition)_ | Active | Closed Source | Basic Containers, file storage, `SEARCH`, `PATCH` | Yes | Yes | Yes | Yes | Not Planned | Yes | Yes | Yes | 
[OpenLink node-solid-server](https://github.com/OpenLinkSoftware/node-solid-server) | Active | Open Source | Basic Containers, file storage | Proxy | Yes | Yes | Yes | No | Yes | Yes | Yes | 
[rww-play](https://github.com/read-write-web/rww-play) | Active | Open Source | Basic Containers, file storage, `SEARCH` | Proxy | Yes | Yes | No | No | N/A | Yes | ? | 

### Actively maintained

#### [gold](https://github.com/linkeddata/gold)
*gold is in bugfix/maintenance mode and no longer under active development; the team is focusing on LDNode.*
Reference Solid platform server written in Go.
See [databox.me](https://databox.me/) for an example instance.

#### [node-solid-server](https://github.com/solid/node-solid-server/)
Reference Solid platform server written in Node.js/Express.

#### [OpenLink Virtuoso](http://virtuoso.openlinksw.com/) Enterprise Edition
More specifically, the WebDAV File System Module a/k/a OpenLink Data Spaces (ODS) Layer.  [ODS](http://ods.openlinksw.com/owiki/wiki/ODS) is a Data Space Shim built around [Virtuoso](https://virtuoso.openlinksw.com/)'s WebDAV layer that adheres to Solid conventions of —
* Identity — via WebID
* Identity Verification (or Authentication) — via WebID-TLS or WebID-OIDC _(WebID-OIDC is still a work-in-progress)_
* Document Access Controls (or Authorization) — via WebACLS or WAC
* Read-Write Operations on Documents — via HTTP `PATCH` using `application/sparql-update` payloads

Minimum installation atop basic Virtuoso (Enterprise Edition only) is Virtuoso Authentication Layer (VAL), ODS-Framework, and ODS-Briefcase VADs.

#### [OpenLink node-solid-server](https://github.com/OpenLinkSoftware/node-solid-server)
Fork of the reference Solid platform server written in Node.js/Express.

#### [rww-play](https://github.com/read-write-web/rww-play)
LDP-compliant Read-Write-Web server written in Scala/Play/akka.

### Inactive

#### [ldphp](https://github.com/linkeddata/ldphp)
LDP PHP server, implementing LDP Basic Containers and file serving.
Not implemented: WAC, WebID-RSA, or WebID-Delegation.

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
