# Ergo Licensing Policy

In order to ensure an open source project is actually open and re-usable in a legal sense, 
it’s critical that licensing information is clear. 
Repositories in the `ergoplatform` and `ScorexFoundation` organizations should all follow this policy 
for licensing their contents.

Unless there is a particular reason to use a different licensing structure, please use 
the following for new projects.

All software code, documentation and non-code resources (e.g. logos and imagery) should be licensed under 
the CC0 1.0 Universal Public Domain Dedication license. 
An [easy-to-read, linkable description](https://creativecommons.org/publicdomain/zero/1.0/) 
and canonical license text in [HTML](https://creativecommons.org/publicdomain/zero/1.0/legalcode) 
and [plain text](https://creativecommons.org/publicdomain/zero/1.0/legalcode.txt) can be found at 
the Creative Commons website.

## Attaching a License

When licensing a project, be sure to:

1. Name the license and provide a link to it from the project README under the heading “license.” Example:

    ```md
    ## License
    
    **<LICENSE NAME>**. See [LICENSE file](./LICENSE) for details.
    ```

2. For software that will be redistributed, the full text of the license(s) **must** be in a file named 
`LICENSE` in the repository root. Other projects **should** do this, too, but their readmes can alternatively 
link to a separate license document, like this: [CC0 1.0 Universal Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/).


## Contributor Licensing (DCO)

We manage contributor licensing via a *Developer Certificate of Origin (DCO).* 
All commits with new code from any contributor **must** include a DCO signoff trailer. 
See the [contributing guide](CONTRIBUTING.md#a-license-and-a-signed-off-by-trailers-are-required) 
for more details. Commits with extremely trivial or changes or that do not change content (e.g. merge commits) are excepted.

If you’re setting up a new repository, make sure the README includes a link to our contribution guidelines 
so people can find information about the DCO signoff.
