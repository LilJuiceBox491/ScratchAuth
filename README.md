| :warning:  ScratchAuth is now deprecated. It is recommended to convert to [sv³](https://github.com/LilJuiceBox491/sv3) ASAP, as ScratchAuth will no longer be maintained. All issues, PRs, e.t.c should be moved to sv³ to avoid false stream commits.   |
|-----------------------------------------|

# ScratchAuth

A next-generation alternative to [ScratchVerifier](http://scratchverifier.ddns.net:8888/site) and [SV2](http://sv2-server.herokuapp.com/).  A public server is available at https://scratchauth.liljuicebox491.repl.co.

## API Reference

### `GET /api`

This requests the status of the server.

**Good response**:

```sh
200 OK
```

**Bad response**:

```sh
500 Server Error
```

### `POST /api/verify`

This requests a user's profile to be checked for the code.

**Body:**

```json
{
  "user": "scratch_username"
}
```

**Good response**:

```json
{
  "code": "3Q8Q8UqObPEQocs3UiVHXy2fp2QqcoQVtlu5seN3nb5BZauFTz"
}
```

**Bad response**:

```sh
406 Not Acceptable
```

### `POST /api/verify`

**Body:**

```json
{
  "user": "scratch_username"
}
```

**Good response**:

```sh
200 OK
```

**Bad response**:

```sh
403 Forbidden
```
