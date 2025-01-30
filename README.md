# briefcase_tutorial
repo with starter code etc for creating Windows desktop apps with briefcase

## Setup
To get this up and running please follow these steps:
1. create a virtual env
`virtualenv .venv`
2. activate it
`source .venv/bin/activate`
3. install briefcase
`python -m pip install briefcase`
4. test that all's well by running this in dev mode
`briefcase dev`
5. test that app will work as expected by spinning up the app, using the packaged version of the app code. By default, this targets the current platform’s default output format.
`briefcase run`
6. now that all's well, you can package for your current platform by compiling/building an app installer for your current platform. NB: the expecttaion is that you're doing this either on Windows or Ubuntu, I have no experience with MacOS
`briefcase package`

## CI
the included _.github/workflows/ci.yml_ file will auto create the installer on github as an artifcat using github actions.

## FAQs
1. why don't you have a MacOS example:
A: I don't use MacOs, sorry 🙏. However, the MacOs specific documentation is [here](https://briefcase.readthedocs.io/en/stable/reference/platforms/macOS/index.html). The only differences will be in the MacOs specific directives in the _pyproject.toml_ file. The most important stuf stays the same i.e. directory structure and basic flow of the _toml_ file. You can also modify the generic CI github actions file [here](https://briefcase.readthedocs.io/en/stable/how-to/ci.html#workflow-file-contents) to derive a MacOS specific version
