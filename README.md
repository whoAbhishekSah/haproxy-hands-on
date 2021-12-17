## How to run

1. install haproxy (`brew install haproxy`)

2. start siren servers in docker (`docker-compose up`)

3. Start HAProxy (`haproxy -f ./haproxy.cfg`)

4. Run a vegeta attack for 30sec : (install vegeta `brew install vegeta`)

   - `echo "GET http://localhost:3000/ping" | vegeta attack -duration 30s | vegeta report`

5. Check HAProxy Stats
   `http://localhost:3000/haproxy?stats`
