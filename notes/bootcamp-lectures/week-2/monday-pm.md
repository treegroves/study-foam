# Testing Express
npm i -D jest @types/jest supertest


async call back
async promise (35mins)
  - close test with `return request(server)`
  - `.then` response -> expect ()

`expect.assertions(1)` 

    test(''). () => {
      expect.assertions(1)
      return request(server)
      .send('')
      .then((response) => {
        expect(response.text).toContain('')
      })
    }