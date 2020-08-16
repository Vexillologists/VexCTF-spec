VexCTF Specification
--------------------

**Introduction**

This is the specification for VexCTF, a platform for online capture-the-flag (CTF) games,
where players attempt to collect "flags", strings of text confirming a user has solved
a challenge, to earn points.

This specification may evolve over time, so each version must be tagged with a 
[Semantic Versioning (SemVer)-compliant](https://semver.org) version. Versions
that are currently in development must be suffixed with `+git`. Versions that
are currently a release candidate must be suffixed with `+rc<release candidate number>`.

**Copyright notice**

Copyright &copy; 2020-present, Vexillologists

This specification is licensed under the CC-BY-SA-4.0 license (as can be seen in the file
[`LICENSE-SPEC`](https://github.com/Vexillologists/VexCTF-spec/blob/master/LICENSE-SPEC)
or at [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/))

Its associated code is licensed under the MIT license (as can be seen in the file
[`LICENSE-CODE`](https://github.com/Vexillologists/VexCTF-spec/blob/master/LICENSE-CODE)
or at [https://spdx.org/licenses/MIT.html](https://spdx.org/licenses/MIT.html)).

Your use of this Specification may be subject to other third party rights. THIS SPECIFICATION IS PROVIDED “AS IS.” The contributors expressly disclaim any warranties (express, implied, or otherwise), including implied warranties of merchantability, non‐infringement, fitness for a particular purpose, or title, related to the Specification. The entire risk as to implementing or otherwise using the Specification is assumed by the Specification implementer and user. IN NO EVENT WILL ANY PARTY BE LIABLE TO ANY OTHER PARTY FOR LOST PROFITS OR ANY FORM OF INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES OF ANY CHARACTER FROM ANY CAUSES OF ACTION OF ANY KIND WITH RESPECT TO THIS SPECIFICATION OR ITS GOVERNING AGREEMENT, WHETHER BASED ON BREACH OF CONTRACT, TORT (INCLUDING NEGLIGENCE), OR OTHERWISE, AND WHETHER OR NOT THE OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

**Conformance**

A conforming VexCTF implementation must fulfill all normative requirements. Requirements for conformance are described in this document via both descriptive assertions and key words with clearly defined meanings.

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in the normative portions of this document are to be interpreted as described in IETF RFC 2119. These key words may appear in lowercase and still retain their meaning unless explicitly declared as non‐normative.

A conforming VexCTF implementation may provide additional functionality, only where such functionality would not be explicitly disallowed or would otherwise result in non-conformance.

**Non-Normative Portions**

All contents of this document are normative except portions explicitly declared as non-normative.


Examples in this document are non-normative, and are presented to aid
understanding of introduced concepts and the behavior of normative portions of
the specification. Examples are either introduced explicitly in prose
(e.g. "for example") or are set apart in example or counter-example blocks,
like this:

```example
This is an example of a non-normative example.
```

```counter-example
This is an example of a non-normative counter-example.
```

Notes in this document are non-normative, and are presented to clarify intent,
draw attention to potential edge-cases and pit-falls, and answer common
questions that arise during implementation. Notes are either introduced
explicitly in prose (e.g. "Note: ") or are set apart in a note block, like this:

Note: This is an example of a non-normative note.
