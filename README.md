

# cloudflared-access-tcp

GitHub Action for establishing a Cloudflare Access TCP tunnel using cloudflared (Linux amd64 only).


## Example usage

```yaml
jobs:
  tunnel:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Start Cloudflare Access TCP tunnel
        uses: acosoft/cloudflared-access-tcp@2025.11.1-linux-amd64
        with:
          hostname: ${{ secrets.CF_TUNNEL_HOST }}
          url: tcp://127.0.0.1:6443
          id: ${{ secrets.CF_ACCESS_CLIENT_ID }}
          secret: ${{ secrets.CF_ACCESS_CLIENT_SECRET }}
```

This version of the action uses cloudflared version 2025.11.1 for Linux amd64.

## Inputs
| Name     | Description                                      | Required |
|----------|--------------------------------------------------|----------|
| hostname | Cloudflare Access application hostname                     | yes      |
| url      | Local TCP URL to forward to (e.g. tcp://localhost:6443)    | yes      |
| id       | Cloudflare Access service token client ID                  | yes      |
| secret   | Cloudflare Access service token secret                     | yes      |



## Versioning Policy

Versions follow the format:

  \<cloudflared-version>-\<architecture>

For example:

  acosoft/cloudflared-access-tcp@2025.11.1-linux-amd64

This means the action uses cloudflared version 2025.11.1 for Linux amd64.

## Contributing

Contributions are welcome! If you have suggestions for improvements, bug reports, or want to add new features, feel free to open an issue or submit a pull request.

## Support

This is an unofficial action. Not affiliated with or endorsed by Cloudflare. For support or questions, please open an issue in this repository or [contact me on LinkedIn](https://linkedin.com/in/acosoft).
