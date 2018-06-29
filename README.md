# solid-platform
[![](https://img.shields.io/badge/project-Solid-7C4DFF.svg?style=flat-square)](https://github.com/solid/solid)

Servers, Tools and packages built on the
[Solid platform](https://github.com/solid/solid-spec).
(See also [solid-apps](https://github.com/solid/solid-apps) for a list of
end-user applications).

## Servers
Actively maintained.  (Note -- you will need to scroll the table to see all columns!)

Name | Project Status | [LDP](https://www.w3.org/TR/ldp/) | [CORS](https://github.com/solid/solid-spec/blob/master/recommendations-server.md) | [WebID](https://github.com/solid/solid-spec/blob/master/solid-webid-profiles.md) IdP | [WebID-TLS](https://github.com/solid/solid-spec/blob/master/authn-webid-tls.md) | [WebID-OIDC](https://github.com/solid/webid-oidc-spec) | [WebID-RSA](https://github.com/solid/solid/blob/master/proposals/auth-webid-rsa.md) | WebID-TLS + Delegation | [WAC](https://github.com/solid/web-access-control-spec) | [WSS](https://github.com/solid/solid-spec/blob/master/api-websockets.md) | Open Source |
-----|-----|:----:|:--------------:|:---------:|:----------:|:---------:|:----------------:|:---:|:---:|:-------:|
[gold](https://github.com/linkeddata/gold) | Bugfix/Maintenance | Basic Containers, file storage | Proxy | Yes | Yes | No | Yes | Yes | Yes | Yes | Yes |
[node-solid-server](https://github.com/solid/node-solid-server/) | Active Development | Basic Containers, file storage | Proxy | Yes | Yes | Yes | No | In Progress | Yes | Yes | Yes |
[OpenLink Virtuoso](http://virtuoso.openlinksw.com/) _(Enterprise Edition)_ | Active Development | Basic Containers, file storage, SEARCH, PATCH | Yes | Yes | Yes | In Progress | Not Planned | Yes | Yes | Yes | No |
[rww-play](https://github.com/read-write-web/rww-play) | Active Development | Basic Containers, file storage, SEARCH | Proxy | Yes | Yes | No | No | N/A | Yes | ? | Yes |

### Actively maintained.

#### [gold](https://github.com/linkeddata/gold)
*No longer under active development (the team is focusing on LDNode),
gold is in bugfix/maintenance mode.*
Reference Solid platform server written in Go.
See [databox.me](https://databox.me/) for an example instance.

#### [node-solid-server](https://github.com/solid/node-solid-server/)
Reference Solid platform server written in Node.js/Express.

#### [OpenLink Virtuoso](http://virtuoso.openlinksw.com/)
More specifically, the WebDAV File System Module a/k/a OpenLink Data Spaces (ODS) Layer.  [ODS](http://ods.openlinksw.com/owiki/wiki/ODS) is a Data Space Shim built around [Virtuoso](https://virtuoso.openlinksw.com/)'s WebDAV layer that adheres to Solid conventions of —
* Identity — via WebID
* Identity Verification (or Authentication) — via WebID-TLS or WebID-OIDC _(WebID-OIDC is still a work-in-progress)_
* Document Access Controls (or Authorization) — via WebACLS or WAC
* Read-Write Operations on Documents — via HTTP PATCH using `application/sparql-update` payloads

Minimum installation atop basic Virtuoso (Enterprise Edition only) installation is Virtuoso Authentication Layer (VAL), ODS-Framework, and ODS-Briefcase VADs.

#### [rww-play](https://github.com/read-write-web/rww-play)
LDP-compliant Read-Write-Web server written in Scala/Play/akka.


### Legacy Servers
No longer actively maintained.

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
