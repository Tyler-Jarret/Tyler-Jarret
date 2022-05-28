# Steps to use Ignite to scaffold a sovereign blockchain specializing in Non-Fungible Records

Using Ignite CLI:

```sh
ignite scaffold chain chain-name --address-prefix chai
```

Move the `config.yml` from the main folder into the newly created folder for the chain.

```sh
> git add .
> git commit -a
```

Add a commit message mentioning the movement and modification of the config file.

```sh
> ignite scaffold module NFR --dep account,bank
> git add .
> git commit -a
```

> _Commit Message:_ "Scaffold Module: NFR (Non-Fungible Record)"

```sh
> ignite scaffold type Collection collection_id name symbol description uri uri_hash minter --module NFR
```

Manually find the `collection.proto` file and adjust the `collection_id` parameter from `string` to `uint`.

```sh
> git add .
> git commit -a
```

> _Commit Message:_ "Scaffolded Type: Collection, adjust collection_id from string to uint"

```sh
> ignite scaffold type NFR collection_id:collectionId nft_id uri uri_hash original_owner minter
```

Manually find the `NFR.proto` and ensure that the `collection_id` is a Type of `collectionId`.

```sh
> git add .
> git commit -a
```

> _Commit Message:_ "Scaffolded Type: NFR"
