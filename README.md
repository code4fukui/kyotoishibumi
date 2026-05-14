# Kyoto Ishibumi Map (いしぶみマップ)

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

An interactive web map of 1,470 stone monuments (*ishibumi*) in and around Kyoto, built using open data from Kyoto City and the [egmapjs](https://github.com/code4fukui/egmapjs) library.


![Screenshot of Kyoto Ishibumi Map](kyotoishibumimap.jpg)


## Demo

**[https://code4fukui.github.io/kyotoishibumi/](https://code4fukui.github.io/kyotoishibumi/)**

## Features

-   **Interactive Map**: Displays the locations of 1,470 stone monuments.
-   **Detailed Information**: Click any monument icon to view a popup with:
    -   Official monument number
    -   Name (links to the official Kyoto City detail page)
    -   Address
    -   [Geo3x3](https://taisukef.github.io/Geo3x3/) location code (links to a Geo3x3 map)
-   **Geolocation**: A "現在位置へ移動" (Go to Current Location) button centers the map on your current position.

## Data Source

This application uses the "Stone Monument List" (石碑リスト) provided by the [Kyoto City Open Data Portal](https://data.city.kyoto.lg.jp/node/14455).

A local copy of the data, [ishibumi-data-281211.csv](ishibumi-data-281211.csv), is included in this repository and used by the application to avoid browser CORS (Cross-Origin Resource Sharing) errors when fetching from the original source.

## Getting Started (Local Development)

This is a static web application that can be run locally. A local web server is required to handle ES module imports correctly due to browser security policies.

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/code4fukui/kyotoishibumi.git
    cd kyotoishibumi
    ```

2.  **Start a local web server.** If you have Python installed, you can use:
    ```sh
    # Python 3
    python -m http.server
    ```
    Or for Node.js, you can use a package like `http-server`:
    ```sh
    npx http-server
    ```

3.  **Open the application** in your browser at the URL provided by the server (e.g., `http://localhost:8000`).

## Attribution

-   **App:** [全1470個所 いしぶみマップ](https://fukuno.jig.jp/3151) CC BY Taisuke Fukuno ([@taisukef](https://github.com/taisukef))
-   **Data:** [CC BY いしぶみリスト | 京都市オープンデータポータルサイト](https://data.city.kyoto.lg.jp/node/14455)
-   **Library:** [egmapjs](https://github.com/code4fukui/egmapjs) (MIT License)

## License

This project is available under the [MIT License](LICENSE).