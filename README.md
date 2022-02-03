# assignment2-Yerramsetty
# thaarani yerramsetty
#### Brew buzz

**Brew buzz** is a coffee shop which is located very near my house.It is situated on national highway.Food here tastes very good,mainly i love **cappuccino** and **velvet butter cookies** here.Prices are also are pretty much affordable.
***
### Address of Brew Buzz
1. Brew buzz is a coffee shop which makes the best coffee in the town.
2. It is situated just 5 miles away from the Gannavaram Airport,Vijayawada,Andhra Pradesh.
    1. General mode of transportations for this coffee shop are auto and buses but personal vehicles are more preferrable.
    2. As it is situated very near to airport,it is very convinient to hangout there after a long tiring flight.
3. Apart from tasty food and coffee this place has high hygienic valves.
* Dragon Chicken is recommended 
* Schewzan Chicken Fried Rice
* French Fries
* Cappuccino

[About me](ABOUTME.md)
***
### List of sports that are recommended 
| Activity Name | Place Recommended | Cost of the equipment |
|---|---|---|
| Throw Ball | Throw ball court | $15 |
| Tennikoit | Ground | $8 |
| Chess | Indoor | $12 |
| Yoga | Indoor and outdoor | $10 |
***
### Quotations for motivation
>"To produce a mighty book, you must choose a mighty theme."-*Herman Melville*

> "I can shake off everything as I write; my sorrows disappear, my courage is reborn."-*Anne Frank*
***
### Code Fencing
>Dijkstra's algorithm is an algorithm for finding the shortest paths between nodes in a graph, which may represent, for example, road networks. It was conceived by computer scientist Edsger W. Dijkstra in 1956 and published three years later.<https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm>
```
const int INF = 1000000000;
vector<vector<pair<int, int>>> adj;

void dijkstra(int s, vector<int> & d, vector<int> & p) {
    int n = adj.size();
    d.assign(n, INF);
    p.assign(n, -1);
    vector<bool> u(n, false);

    d[s] = 0;
    for (int i = 0; i < n; i++) {
        int v = -1;
        for (int j = 0; j < n; j++) {
            if (!u[j] && (v == -1 || d[j] < d[v]))
                v = j;
        }

        if (d[v] == INF)
            break;

        u[v] = true;
        for (auto edge : adj[v]) {
            int to = edge.first;
            int len = edge.second;

            if (d[v] + len < d[to]) {
                d[to] = d[v] + len;
                p[to] = v;
            }
        }
    }
}
```
<https://cp-algorithms.com/graph/dijkstra.html>




