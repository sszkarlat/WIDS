# Projekt: Bezpieczeństwo Bezprzewodowych Sieci Komputerowych – Przegląd i test wybranych rozwiązań WIDS 🛡️📡

Niniejszy projekt stanowi kompleksowy przegląd oraz praktyczne testy wybranych systemów WIDS (Wireless Intrusion Detection System). Celem było zbadanie ich możliwości w zakresie monitorowania, wykrywania intruzów i analizy zagrożeń w sieciach bezprzewodowych.

## Autorzy

*   Michał Dziarkowski
*   Wojciech Matuszyński
*   Aleksandra Rząca
*   Szymon Szkarłat

## Testowane Rozwiązania WIDS

W ramach projektu przeanalizowano i przetestowano następujące narzędzia:

1.  **Snort**:
    *   Open-source'owy IDS, dostosowany do pracy jako WIDS.
    *   Konfiguracja oparta o plik `snort.conf` oraz zestawy reguł (`.rules`).
    *   Wymagał dodatkowych narzędzi (np. `aircrack-ng`) do przełączenia interfejsu w tryb monitor.
2.  **Suricata**:
    *   Nowoczesny, wielowątkowy IDS/IPS typu open-source.
    *   Konfiguracja za pomocą pliku `suricata.yaml` i reguł.
    *   Testowano m.in. ekstrakcję plików i generowanie logów `.pcap`.
3.  **Pulledpork**:
    *   Narzędzie pomocnicze dla Snorta i Suricaty, automatyzujące zarządzanie regułami (pobieranie, aktualizacja).
4.  **Splunk Enterprise + Splunk Stream**:
    *   Komercyjne rozwiązanie big-data wykorzystane jako WIDS.
    *   Splunk Stream jako sniffer sieciowy.
    *   Architektura obejmowała Independent Splunk Forwarder (ISF) i komunikację przez HEC (HTTP Event Collector).
    *   Prezentacja danych za pomocą wbudowanych dashboardów Splunka.
5.  **Kismet**:
    *   Darmowe, open-source'owe narzędzie dedykowane do monitorowania sieci bezprzewodowych.
    *   Konfiguracja alertów przez `kismet_alerts.config`.
    *   Intuicyjny interfejs graficzny.
    *   Przeprowadzono symulacje ataków (Beacon Flooding, Deauthentication, AP spoofing) i analizowano alerty (np. `NOCLIENTMFP`, `DEAUTHFLOOD`, `ADVCRYPTCHANGE`).

## Cele Projektu

*   **Przegląd:** Teoretyczne zapoznanie się z każdym z wybranych rozwiązań.
*   **Instalacja i Konfiguracja:** Praktyczne przejście przez proces instalacji i podstawowej konfiguracji.
*   **Testowanie:** Weryfikacja działania systemów poprzez:
    *   Monitorowanie ruchu w sieci bezprzewodowej.
    *   Generowanie i symulację typowych ataków (gdzie to możliwe i adekwatne do narzędzia).
    *   Analizę wykrytych zdarzeń, alertów i logów.
*   **Porównanie:** Wskazanie kluczowych cech, zalet, wad oraz potencjalnych scenariuszy użycia dla każdego z narzędzi.

## Główne Aspekty Analizy

Dla każdego systemu starano się ocenić:

*   **Dostępność:** (open-source, komercyjne, darmowe wersje)
*   **Łatwość Instalacji i Konfiguracji:**
*   **Skuteczność Wykrywania:** (na podstawie przeprowadzonych testów)
*   **Zalety i Wady:**

## Podsumowanie

Projekt dostarcza praktycznych informacji na temat funkcjonalności, konfiguracji oraz możliwości wybranych systemów WIDS. Wyniki testów i analizy pozwalają na lepsze zrozumienie specyfiki każdego z narzędzi, co może być pomocne przy wyborze odpowiedniego rozwiązania do zabezpieczania sieci bezprzewodowych w różnych środowiskach.
