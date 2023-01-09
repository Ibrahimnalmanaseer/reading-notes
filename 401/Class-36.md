# Data Fetching

## What is SWR?

SWR stands for `stale-while-revalidate`, a HTTP cache invalidation strategy popularized by HTTP RFC 5861. It basically means that it performs data fetching in 3 steps:

- Returns cached data first (stale)
- Sends the fetch request (revalidate)
- Returns the up-to-date data


It is a layer built on top of Fetch API and therefore provides additional features on top of just data fetching. These features include caching, pagination, auto revalidation and more.


## Why use SWR?

1. **Built-in Cache + Real-Time Experience**

 the user sees the cached (stale) data first and requests are automatically being cached. Components will always be constantly updated with the most recent data, ensuring UI will always be fast and reactive.
 
 2. **Auto Revalidation**

SWR ensures that the user sees the most up-to-date data. So even with multiple tabs or windows, the data is always fresh and in sync when the window/tab is refocused.

3. **Pagination**

Instead of having to write your own logic with Fetch or Axios to paginate data or create an infinite loading UI for your app, SWR provides a simple Hook called useSWRInfinite to handle this for you.


## Example Usage of SWR in React

```
import useSWR from "swr";
import "./App.css";

function App() {
  const fetcher = (...args) => fetch(...args).then((res) => res.json());

  // fetch data
  const { data, error } = useSWR(
    "https://jsonplaceholder.typicode.com/todos/1",
    fetcher
  );

  if (error) return <div>failed to load</div>;
  
  if (!data) return <div>loading...</div>;

  // render data
  return (
    <div className="App">
      <h2>{data.title}</h2>
      <p>UserId: {data.userId}</p>
      <p>Id: {data.id}</p>
      {data.completed? <p>Completed</p> : <p>Not Completed</p>}
    </div>
  );
}

export default App;
```
