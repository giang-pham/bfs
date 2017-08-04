# bfs
Node :start, Node :finish

Map visited, Map previous

List path, Queue q;

Node current = start;
q.add(current);
visited.put(current, true);

// explore the possible paths using breadth-depth on a tree
while q is not empty
    current = q.pop();
    if (current is destination){
        break;
    } else {
        for each node in current.getNeighbours() {
            if(node is not visited) {
                q.add(node);
                visited.put(node, true);
                previous.put(node, current);
            }
        }
    }
}

//travese back using previous node map
Node node = destination;
do 
  node = previous.get(node);  
  path.add(node);
while node is not null:

sysout(path);
