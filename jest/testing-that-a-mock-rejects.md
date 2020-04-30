# In order to test that a jest mock rejects properly the await needs to go on the expect

```
describe('when the pg connection fails',()=> {
  beforeEach(() => {
    const returnValue = new Error('This should fail')
    mockedPostgresConnection.manyOrNone.mockReturnValue(Promise.reject(returnValue))
})

it('should throw an exception', async ()=> {
  await expect(subject.findAllReplicationJobs()).rejects.toThrow()
  ...
})
```
**Note that the await is on the `expect` and the `rejects` property**
