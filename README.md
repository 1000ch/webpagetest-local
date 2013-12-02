# webpagetest-local

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
$ git clone https://github.com/WPO-Foundation/webpagetest.git
$ git clone https://github.com/1000ch/webpagetest-local.git
```
### Boot vagrant

```sh
$ vagrant up --provision
```

### Browse `http://192.168.33.10:8080`

## License

MIT.