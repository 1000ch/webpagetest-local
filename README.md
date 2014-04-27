# webpagetest-private

## About

To debug [WebPagetest Private Instance](https://github.com/WPO-Foundation/webpagetest) at local.

## Premise

### [ansible](http://www.ansibleworks.com/) is required on your Mac.

```sh
$ brew install ansible
```

## Usage

### Clone repositories

```sh
$ git clone https://github.com/bayandin/webpagetest-private.git
```

### Boot vagrant

```sh
$ vagrant up --provider=parallels
```

### Browse `http://192.168.33.33:8080`

## License

MIT.
