# Mocking multiple named exports in Jest

Mock it:
```
jest.mock('path/to/some/module', () => ({
    someNamedExportFromModule: jest.fn()
  }))
```
Then import it:
```
import {someNamedExportFromModule} from 'path/to/some/module'
```
Setup value to return:
```
someNamedExportFromModule.mockReturnValue('someValue')
```
