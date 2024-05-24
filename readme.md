function startGame() {
    // Oyun başladığında, mayın sayısını gösteren elemente "minesCount" değerini yazdır.
    document.getElementById("mines-count").innerHTML = minesCount;

    // Satır (r) döngüsü: Oyun tahtasının satırlarını oluşturmak için bu döngü kullanılır.
    for (let r = 0; r < rows; r++) {
        let row = []; // Her satır için bir dizi oluşturulur. Bu dizi satırdaki hücreleri temsil edecek.

        // Sütun (c) döngüsü: Her satırın içindeki sütunları oluşturmak için bu döngü kullanılır.
        for (let c = 0; c < columns; c++) {
            // Her hücre için bir "div" elementi (kutu) oluşturulur.
            let tile = document.createElement("div");

            // Her hücrenin "id" özelliği, hücrenin konumunu temsil eder (örneğin, "2-2" hücresi 2. satır ve 2. sütundadır).
            tile.id = r.toString() + "-" + c.toString();

            // Oluşturulan hücre "board" elementine eklenir, böylece görüntülenir.
            document.getElementById("board").append(tile);

            // Oluşturulan hücre, bu satırdaki hücreleri temsil eden "row" dizisine eklenir.
            row.push(tile);
        }

        // Oluşturulan satır dizisi, "board" dizisine eklenir.
        board.push(row);
    }
}
