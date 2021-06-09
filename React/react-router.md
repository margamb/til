#### install

- npm install react-router
- npm install react-router-dom

#### index.js

```jsx
import ReactDOM from 'react-dom';
import { HashRouter } from 'react-router-dom';

ReactDOM.render(
  <React.StrictMode>
    <HashRouter>
      <App />
    </HashRouter>
  </React.StrictMode>,
  document.getElementById('root')
);
```

#### App.js

```jsx
import { Switch, Route } from 'react-router-dom';

 return (
    <div className="App">
      <Switch>
        <Route exact path="/">
          <Movies movies={movieAPI} />
        </Route>
        <Route path="/detail/:id" component={renderMovieDetails} />

        <Route path="/booking/:id" component={renderBooking} />

        <Route path="/ticket/:id" component={renderTicket} />
      </Switch>
      <Footer />
    </div>
  );
}
```

#### Link

```jsx
import { Link } from 'react-router-dom';

<Link to="/" style={{ textDecoration: 'none' }} onClick={handleReset}>
  <IconReset />
</Link>;
```
