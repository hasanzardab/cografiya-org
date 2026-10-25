# Coğrafiya.org

cografiya-org dizaynı (navy / mavi, Inter şrifti) ilə GeoAtlas-ın bütün məzmunu birləşdirilib. Server və ya build tələb etmir — GitHub Pages-də birbaşa işləyir.

## Struktur
- `index.html` — ana səhifə (cografiya-org bölmələri + ölkə siyahısı + statistika)
- `assets/css/style.css` — ortaq stil; sonundakı **"COĞRAFİYA.ORG DİZAYNI"** bloku rəngləri, şrifti, header, hero və footer-i idarə edir
- `assets/js/` — `countries-data.js` (ölkə reyestri və menyu), `site.js` (menyu, axtarış, gecə rejimi), ölkə rayon məlumatları, testlər
- `countries/`, `oyunlar/`, `testler/`, `simulyasiya/`, `tetbiqler/`, `haqqimizda/`, `elaqe/`, `img/`, `gif/`

## Yeni ölkə əlavə etmək
`countries/<ölkə>.html` və `assets/js/<ölkə>-regions.js` yarat, sonra `assets/js/countries-data.js` içindəki `SITE_COUNTRIES` massivinə bir sətir əlavə et — menyu və siyahılar avtomatik yenilənir.

## Rəngləri dəyişmək
`assets/css/style.css` sonundakı `:root` (gündüz) və `:root[data-theme="dark"]` (gecə) dəyişənləri.

## GitHub Pages
Faylları repository-nin kökünə yüklə → **Settings → Pages → Deploy from a branch → main / (root)**.

## Qeydlər
- `assets/js/cloudflare-worker.js`, `wrangler.toml`, `apps-script-leaderboard.gs` backend faylları GeoAtlas-dan olduğu kimi saxlanılıb (saytda işləmirlər, ayrıca deploy olunur).
- `icon/favicon.png` GeoAtlas arxivində yox idi; istəsən `icon/` qovluğu yaradıb əlavə et.
