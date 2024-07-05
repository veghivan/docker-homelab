# Otthoni Szerver Konfigurációs Áttekintés

Elő website: https://main.ivuserver.duckdns.org

Ez a tároló tartalmazza a Docker compose fájlokat egy átfogó otthoni szerver környezethez. Az alábbiakban minden szolgáltatás részletes leírását találod.
![PNG](/images/grafika.png)


## Szolgáltatások

### Pihole-Unbound
- **Leírás**: DNS megoldó szolgáltatás hirdetésblokkolóval kombinálva.
- **Portok**: 53 (DNS), 5335 (Unbound), 4443 (HTTPS)

### DuckDNS
- **Leírás**: Dinamikus DNS szolgáltatás konfigurációja.
- **Frissítési intervallum**: Minden 5 percben.

### MC-Server
- **Leírás**: Minecraft szerver.
- **Portok**: 25565 (Alapértelmezett Minecraft port), 19132 (Bedrock kiadás)

### Plex
- **Leírás**: Médiaszerver szoftver, amely szervezi a videókat, zenéket és fotókat a személyes média könyvtárakból és továbbítja azokat a média eszközökre.
- **Port**: 32400 (WebUI), 1900 (DLNA), 8324 (Plex Companion)

### Nginx Proxy Manager
- **Leírás**: Kezeli és továbbítja a bejövő hálózati forgalmat a különböző otthoni hálózaton futó szolgáltatásokhoz.
- **Portok**: 80 (HTTP), 443 (HTTPS), 81 (Kezelő felület)

### Portainer
- **Leírás**: Docker konténer kezelő eszköz.
- **Port**: 9000

### NetData
- **Leírás**: Valós idejű teljesítményfigyelő eszköz.
- **Port**: 19999

### WG-EASY (WireGuard VPN)
- **Leírás**: VPN szerver, amely a WireGuard-ot használja a hálózati forgalom biztonságának növelésére.
- **Portok**: 51820 (UDP), 51821 (Kezelés)

### Nextcloud
- **Leírás**: Önálló cloud platform, amely az irányítást a te kezedbe adja.
- **Port**: 80 (HTTP)

### VaultWarden
- **Leírás**: Könnyűsúlyú, Bitwarden-kompatibilis jelszókezelő.
- **Port**: 80 (HTTP)

### qBittorent
- **Leírás**: Torrent letöltő kliens.
- **Portok**: 6881 (BitTorrent), 8000 (Webes felület)

### FileBrowser
- **Leírás**: Web-alapú fájlkezelő eszköz.
- **Port**: 80 (HTTP)

### Surprise
- **Leírás**: Meglepetés.

## Telepítés

A szolgáltatások telepítéséhez konfiguráldd a számodra megfelelő felhasználásra a konténereket, ezt a comopose fájlban és a környezeti változók személyre szabásával teheted meg.
Minden szolgáltatás almappájában a konfigurációt a követően "docker-compose up -d"-paranccsal elindíthatod. (Portainer használata esetén létrehozol egy új stacket, és ott tudod konfigurálni a környezeti változókat)


## Karbantartás

Rendszeres frissítések ajánlottak a biztonság és a funkcionalitás javítása érdekében. Minden szolgáltatás dokumentációja tartalmazza a specifikus karbantartási útmutatókat. 


## Közreműködés

Minden hozzájárulást szívesen fogadunk a konfigurációk javítására vagy új szolgáltatások hozzáadására. Kérjük, tartsd be a meglévő fájlstruktúrát és kódolási szabványokat.
