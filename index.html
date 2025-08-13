
<!-- 
  ðŸ’» Code By Ahmad Mods
  âš ï¸ Change Credit On Your Risk I Add Backdoors On This Code!!!
  ðŸ“ Whatsapp Channel : https://whatsapp.com/channel/0029Vb5faX5ADTOILyh8B83A
  ðŸ”± Telegream Channel : https://t.me/AhmadModsOfficiall
  ðŸ“… Version: 1.0
-->

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SIM DATA-BASE - AHMAD MODS</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Nastaliq+Urdu&display=swap" rel="stylesheet" />
  <style>
    canvas {
      position: fixed; top: 0; left: 0;
      width: 100vw; height: 100vh;
      z-index: 0;
    }
    .urdu-text {
      font-family: 'Noto Nastaliq Urdu', serif;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    .animate-fade-in {
      animation: fadeIn 0.8s ease forwards;
    }
  </style>
</head>
<body class="bg-black text-white font-sans overflow-hidden relative" lang="en">

<canvas id="matrixCanvas" aria-hidden="true"></canvas>

<main class="relative z-10 min-h-screen flex items-center justify-center px-4">
  <section aria-labelledby="main-title" class="bg-gray-900 bg-opacity-80 backdrop-blur-md rounded-2xl shadow-lg p-8 w-full max-w-md animate-fade-in" role="main">
    <header class="text-center mb-6">
      <h1 id="main-title" class="text-4xl font-bold text-green-400">Ahmad-Mods</h1>
      <h2 class="text-xl text-blue-300 mt-2">ðŸ” Sim Data-Base</h2>
    </header>

    <form method="POST" class="space-y-4" aria-describedby="form-description">
      <p id="form-description" class="sr-only">Enter your phone number (03xxxxxxxxx) or CNIC (13 digits) and submit to search the SIM database.</p>
      <label for="inputValue" class="sr-only">Phone Number or CNIC</label>
      <input
        type="text"
        id="inputValue"
        name="inputValue"
        placeholder="03xxxxxxxxx or 13-digit CNIC"
        pattern="(03\d{9}|\d{13})"
        title="Enter a phone number starting with 03 followed by 9 digits, or a 13-digit CNIC number"
        autocomplete="off"
        inputmode="numeric"
        required
        class="w-full p-3 rounded-lg bg-black text-white border border-gray-700 focus:ring-2 focus:ring-green-400 focus:outline-none"
      />
      <button
        type="submit"
        class="w-full bg-blue-500 hover:bg-blue-600 text-white font-semibold p-3 rounded-lg transition duration-200"
      >
        ðŸ”Ž Search
      </button>
    </form>

    <?php
    if ($_SERVER['REQUEST_METHOD'] === 'POST' && isset($_POST['inputValue'])) {
      
        $input = trim($_POST['inputValue']);

        // Validate input: phone OR CNIC
        if (preg_match('/^(03\d{9}|\d{13})$/', $input)) {

            // For phone number, remove leading 0 for API
            if (preg_match('/^03\d{9}$/', $input)) {
                $apiParam = ltrim($input, '0');
            } else {
                // CNIC sent as is
                $apiParam = $input;
            }

            $apiParam = htmlspecialchars($apiParam, ENT_QUOTES, 'UTF-8');
            $url = 'https://ahmadmodstools.online/Apis/Simdata.php?num=' . urlencode($apiParam);

            $ch = curl_init($url);
            curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
            curl_setopt($ch, CURLOPT_TIMEOUT, 10);
            $response = curl_exec($ch);
            $httpCode = curl_getinfo($ch, CURLINFO_HTTP_CODE);
            curl_close($ch);

            echo '<section class="mt-6" aria-live="polite" aria-atomic="true">';

            if ($httpCode === 200 && $response !== false) {
                $data = json_decode($response, true);

                if (json_last_error() !== JSON_ERROR_NONE) {
                    echo '<div class="bg-red-900 text-red-300 p-4 rounded-lg">âŒ Invalid JSON: ' . htmlspecialchars(json_last_error_msg()) . '</div>';
                } elseif (!empty($data)) {
                    // Handle multiple entries
                    if (isset($data[0]) && is_array($data[0])) {
                        echo '<h3 class="text-cyan-400 text-lg font-semibold mb-2">ðŸ”Ž Multiple SIM Data Found</h3>';
                        foreach ($data as $entry) {
                            $name = htmlspecialchars($entry['Name'] ?? 'Not found');
                            $cnic = htmlspecialchars($entry['CNIC'] ?? 'Not found');
                            $numbers = htmlspecialchars($entry['Numbers'] ?? 'Not found');
                            $address = htmlspecialchars($entry['Address'] ?? 'Not found');

                            if ($numbers !== 'Not found' && $numbers[0] !== '0') {
                                $numbers = '0' . $numbers;
                            }

                            echo "<div class='bg-gray-800 p-4 rounded-lg shadow-lg space-y-2 text-sm mb-4'>";
                            echo "<p><strong>ðŸ‘¤ Name:</strong> $name</p>";
                            echo "<p><strong>ðŸ†” CNIC:</strong> $cnic</p>";
                            echo "<p><strong>ðŸ“ž Number:</strong> $numbers</p>";
                            echo "<p><strong>ðŸ“ Address:</strong> $address</p>";
                            echo "</div>";
                        }
                    } else {
                        // Single entry
                        $name = htmlspecialchars($data['Name'] ?? 'Not found');
                        $cnic = htmlspecialchars($data['CNIC'] ?? 'Not found');
                        $numbers = htmlspecialchars($data['Numbers'] ?? 'Not found');
                        $address = htmlspecialchars($data['Address'] ?? 'Not found');

                        if ($numbers !== 'Not found' && $numbers[0] !== '0') {
                            $numbers = '0' . $numbers;
                        }

                        $textData = "ðŸ” SIM Data Found\nðŸ‘¤ Name: $name\nðŸ†” CNIC: $cnic\nðŸ“ž Number: $numbers\nðŸ“ Address: $address";
                        $textDataJs = json_encode($textData, JSON_HEX_TAG | JSON_HEX_APOS | JSON_HEX_QUOT | JSON_HEX_AMP);

                        echo <<<HTML
                        <div class="bg-gray-800 p-4 rounded-lg shadow-lg space-y-2 text-sm">
                          <h3 class="text-center text-cyan-400 text-lg font-semibold">ðŸ”Ž SIM Data Found</h3>
                          <p><strong>ðŸ‘¤ Name:</strong> {$name}</p>
                          <p><strong>ðŸ†” CNIC:</strong> {$cnic}</p>
                          <p><strong>ðŸ“ž Number:</strong> {$numbers}</p>
                          <p><strong>ðŸ“ Address:</strong> {$address}</p>
                          <div class="space-y-2 pt-2">
                            <button onclick="copyData({$textDataJs})" class="w-full bg-blue-500 hover:bg-blue-600 p-2 rounded-lg" type="button">ðŸ“‹ Copy All Data</button>
                            <button onclick="shareOnWhatsApp({$textDataJs})" class="w-full bg-green-500 hover:bg-green-600 text-black p-2 rounded-lg" type="button">ðŸ“¤ Share on WhatsApp</button>
                          </div>
                        </div>
HTML;
                    }
                } else {
                    echo '<div class="text-center bg-red-900 text-red-300 p-4 rounded-lg">âŒ No data found for this input.</div>';
                }
            } else {
                echo '<div class="text-center bg-red-900 text-red-300 p-4 rounded-lg">âŒ Error fetching data. API may be down.</div>';
            }

            echo '</section>';
        } else {
            echo '<div class="mt-6 bg-red-900 text-red-300 p-4 rounded-lg text-center">âŒ Invalid input format. Enter 03xxxxxxxxx or 13-digit CNIC.</div>';
        }
    }
    ?>

    <a href="https://whatsapp.com/channel/0029VajZpqL7T8bRvUqAU23A" target="_blank" rel="noopener noreferrer">
      <button class="w-full mt-4 bg-green-500 hover:bg-green-600 text-black font-bold p-3 rounded-lg" type="button">ðŸ’¬ Contact Developer</button>
    </a>
  </section>
</main>

<script>
  // Enforce '0' start for phone input if needed
  const inputValue = document.getElementById('inputValue');
  inputValue.addEventListener('input', () => {
    if (/^03/.test(inputValue.value)) {
      if (inputValue.value.length > 0 && inputValue.value[0] !== '0') {
        inputValue.value = '0' + inputValue.value.replace(/^0+/, '');
      }
    }
  });

  function copyData(text) {
    navigator.clipboard.writeText(text).then(() => alert("âœ… Copied to clipboard!"))
      .catch(() => alert("âŒ Unable to copy to clipboard!"));
  }

  function shareOnWhatsApp(text) {
    const url = "https://wa.me/?text=" + encodeURIComponent(text);
    window.open(url, "_blank", "noopener");
  }

  // Matrix background effect
  const canvas = document.getElementById("matrixCanvas");
  const ctx = canvas.getContext("2d");
  
  function resizeCanvas() {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
  }
  resizeCanvas();
  window.addEventListener('resize', resizeCanvas);

  const chars = "01";
  const fontSize = 16;
  let columns = Math.floor(canvas.width / fontSize);
  let drops = Array(columns).fill(1);

  function drawMatrix() {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = "#00f2ff";
    ctx.font = fontSize + "px monospace";

    for (let i = 0; i < drops.length; i++) {
      const char = chars.charAt(Math.floor(Math.random() * chars.length));
      ctx.fillText(char, i * fontSize, drops[i] * fontSize);

      if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
        drops[i] = 0;
      }
      drops[i]++;
    }
  }
  setInterval(drawMatrix, 30);
</script>

</body>
</html>
