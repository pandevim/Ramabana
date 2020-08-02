# Ramabana

Quiz app


## Setup
```bash
$ # Create project container from web image and bind correct directory
$ docker run --interactive --tty \
--name ramabana \
--mount type=bind,source=`pwd`,target=/app \
--publish 3000:3000 \
pandevim/web
```
```bash
/app $ # Template  Next.js app
/app $ npm init next-app ramabana --example "https://github.com/vercel/next-learn-starter/tree/master/learn-starter"
/app $ cd ramabana/
```

## Source Control
```bash
/ramabana $ git remote add origin git@github.com:S2W2/Ramabana.git
/ramabana $ git add .
/ramabana $ git commit -m "initial commit"
/ramabana $ git push -u origin master
```

## Development
```bash
/ramabana $ docker exec -it ramabana bash
/ramabana $ yarn dev
```

## Build
```bash
/ramabana $ docker exec -it ramabana bash
/ramabana $ yarn build
```