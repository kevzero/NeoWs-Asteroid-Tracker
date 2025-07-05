# 🪐 NeoWs Asteroid Tracker (NASA API) in C

A C program that connects to NASA's **NeoWs (Near Earth Object Web Service)** API, downloads data about near-Earth asteroids, and displays it in the terminal in JSON format.

> ⚙️ Uses the `libcurl` library to perform HTTP requests.

## 📷 Sample Output

```
Response from NASA API (near-Earth asteroid data):

{
  "element_count": 12,
  "near_earth_objects": {
    "2025-07-05": [
      {
        "name": "Asteroid 2025 AB1",
        "estimated_diameter": { ... },
        "close_approach_data": [ ... ]
      },
      ...
    ]
  }
}
```

## 📁 Main Files

| File               | Description                                  |
|--------------------|----------------------------------------------|
| `neows_asteroidi.c`| Main C source code of the program             |
| `README.md`        | Project documentation                         |

## 🚀 How to Run

### 1. Install `libcurl` (if not already installed)

On Ubuntu / Debian:

```bash
sudo apt update
sudo apt install libcurl4-openssl-dev
```

### 2. Compile the Program

```bash
gcc neows_asteroidi.c -o neows -lcurl
```

### 3. Run It

```bash
./neows
```

## 🔐 NASA API Key

This project uses NASA’s public **`DEMO_KEY`**, which is free and available to everyone.

| Parameter | Value                          |
|----------|---------------------------------|
| Name     | DEMO_KEY                        |
| Limit    | 30 requests/hour, 50/day        |
| Expiry   | None                            |
| Request  | https://api.nasa.gov            |

> ⚠️ For personal use, you can get your own free API key and replace `"DEMO_KEY"` in the code.

## 🧠 Possible Improvements

- JSON parsing using the `cJSON` library
- Extract asteroid names, speed, and approach distance
- Save output to `.txt` or `.csv` files
- Display data in a better format using `ncurses` or create a GUI using `GTK`
- Add a `Makefile` to simplify compilation

## 📜 License

This project is open source and free to use for educational, scientific, and non-commercial purposes.

## 🙌 Acknowledgments

- [NASA Open APIs](https://api.nasa.gov)
- [libcurl](https://curl.se/libcurl/)
