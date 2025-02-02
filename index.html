<?php
if (!empty($_SERVER['HTTP_X_FORWARDED_FOR'])) {
    $ips = explode(',', $_SERVER['HTTP_X_FORWARDED_FOR']);
    $user_ip = trim($ips[0]); // Отримуємо перший IP з ланцюга
} elseif (!empty($_SERVER['CF-Connecting-IP'])) { // Cloudflare
    $user_ip = $_SERVER['CF-Connecting-IP'];
} else {
    $user_ip = $_SERVER['REMOTE_ADDR'];
}

// API для отримання країни (використовуємо IP користувача)
$api_url = "https://ipinfo.io/{$user_ip}/json?token=fc5b15b45deb91";
$response = @file_get_contents($api_url);
$data = json_decode($response, true);

// Якщо API не відповідає або повернув помилку
if (!$data || !isset($data['country'])) {
    http_response_code(404);
    include "404.html"; // Використовуємо окрему 404 сторінку
    exit();
}

// Отримуємо код країни
$countryCode = strtoupper(trim($data['country']));

// Логування (тимчасово)
file_put_contents("log.txt", "User IP: " . $user_ip . " | Country: " . $countryCode . PHP_EOL, FILE_APPEND);

// Списки країн
$allowedCountries = ["US", "GB", "CA", "DE", "UA"]; // Дозволені країни
$blockedCountries = ["RU", "CN", "KP", "IR"]; // Заборонені країни

// 🔹 Перевіряємо країну
if (in_array($countryCode, $blockedCountries)) {
    http_response_code(404);
    include "404.html";
    exit();
}

if (in_array($countryCode, $allowedCountries)) {
    header("Location: https://penis.is-best.net/");
    exit();
}

// Якщо країна не в списках → 404
http_response_code(404);
include "404.html";
exit();
?>
