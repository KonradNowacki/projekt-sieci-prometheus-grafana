1. Uruchom kontenery komendą: docker-compose up
2. Wejdź na UI Grafany http://localhost:3000
3. W sekcji Data Sources dodaj Prometheusa
4. Kliknij Create Dashboard, zaimportuj dashboard o ID 1860

# Sprawdzenie prometheus
1. Wejdź na UI Prometheusa http://localhost:9090
2. Exec do naszego kontenera, obciążenia producera: docker exec -it load-generator sh
3. Zacznij wywoływać sieć na linux-node komendą: while true; do curl -s linux-node:9100/metrics > /dev/null; sleep 0.1; done
4. W Grafanie i Prometeuszu powinno być widać ruch w polach związanych z netwoekirm i CPU

