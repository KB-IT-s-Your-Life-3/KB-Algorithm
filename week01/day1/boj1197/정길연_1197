package day1.boj1197;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.StringTokenizer;

class Edge{
    int from;
    int to;
    int weight;

    public Edge(int from, int to, int weight) {
        this.from = from;
        this.to = to;
        this.weight = weight;
    }
}

public class 정길연_1197 {

    static int V, E;
    static int[] parent;
    static Edge[] edges;

    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine());

        V = Integer.parseInt(st.nextToken());   // V: 노드
        E = Integer.parseInt(st.nextToken());   // E: 간선
        edges = new Edge[E];

        for (int i = 0; i < E; i++) {
            st = new StringTokenizer(br.readLine());
            int from = Integer.parseInt(st.nextToken());
            int to = Integer.parseInt(st.nextToken());
            int weight = Integer.parseInt(st.nextToken());
            edges[i] = new Edge(from, to, weight);
        }

        // 가중치가 작은거부터 정렬
        Arrays.sort(edges, (e1, e2) -> e1.weight - e2.weight);

        parent = new int[V + 1];
        for (int i = 1; i <= V; i++) {
            parent[i] = i;
        }

        int total = 0;
        int cnt = 0;
        // edge에 연결된 애들은 부모 이어주기
        for (Edge e : edges) {
            if (union(e.from, e.to)) {
                cnt ++;
                total += e.weight;
                if (cnt == V - 1) {
                    break;
                }
            }
        }

        System.out.println(total);
        br.close();
    }

    // 부모 찾기
    private static int find(int x) {
        if (parent[x] != x) {
            return parent[x] = find(parent[x]);
        }
        return x;
    }

    // 부모 체크
    private static boolean union(int a, int b) {
        int aParent = find(a);
        int bParent = find(b);
        if( aParent == bParent) return false;
        parent[bParent] = aParent;
        return true;
    }

}
