# Solar System Calculator

A single-file interactive web tool for building scale models of the solar system and calculating distances between planets.

## Features
- Enter a sun diameter and get all planet diameters and distances to scale
- Calculate the distance between any two solar system objects
- All logic and UI in a single HTML file (no dependencies)

## Usage
Just serve `index.html` with any static web server or open it directly in your browser.

## Example nginx configuration
To serve this app at `https://yourdomain.com/solarsystem/`:

```nginx
server {
    listen 443 ssl;
    server_name yourdomain.com;
    root /var/www/html/solarsystem;

    location /solarsystem/ {
        index index.html;
        try_files $uri $uri/ /solarsystem/index.html;
    }
}
```

- Place `index.html` in `/var/www/html/solarsystem/`
- Adjust `server_name` and `root` as needed

## License
MIT

## Author
Created by [hromp.com](https://hromp.com)
