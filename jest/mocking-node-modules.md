# Mocking Node Modules
*https://jestjs.io/docs/en/manual-mocks#mocking-node-modules

If the module you are mocking is a Node module (e.g.: lodash), the mock should be placed in the __mocks__ directory adjacent to node_modules (unless you configured roots to point to a folder other than the project root) and will be automatically mocked. **There's no need to explicitly call jest.mock('module_name')**.

Scoped modules can be mocked by creating a file in a directory structure that matches the name of the scoped module. For example, to mock a scoped module called @scope/project-name, create a file at __mocks__/@scope/project-name.js, creating the @scope/ directory accordingly.
