# top-ceo-chart

Glassdoor&#39;s Top CEO charts. Annual transition

Source

- https://www.glassdoor.com/Award/Top-CEOs-LST_KQ0,8.htm

Code

```shell
copy(Array.from(document.querySelectorAll(".ceoSingle"), (el, index) => {
  return {
    rank: Number(el.querySelector(".listRank").textContent.replace(/[^\d]+/g, "").trim()),
    ceo: el.querySelector("strong").textContent.trim(),
    ceoImg:  el.querySelector(".ceo").dataset.original,
    company: el.querySelector("div:nth-child(2) > div:nth-child(2) > p:nth-child(2)").textContent.trim(),
    approval:  el.querySelector(".minor").textContent.trim(),
  }
}))
```

Data

[data/us](data/us)

## Usage

- [ ] Write usage instructions

## Changelog

See [Releases page](https://github.com/azu/top-ceo-chart/releases).

## Running tests

Install devDependencies and Run `npm test`:

    npm test

## Contributing

Pull requests and stars are always welcome.

For bugs and feature requests, [please create an issue](https://github.com/azu/top-ceo-chart/issues).

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Author

- azu: [GitHub](https://github.com/azu), [Twitter](https://twitter.com/azu_re)

## License

MIT © azu
