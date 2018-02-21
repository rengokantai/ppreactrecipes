# ppreactrecipes
### Using React Router to Create Basic Routing
BrowserRouter only accept one child.
```
const App = ()=>(
  <BrowserRouter>
    <main>
      <Header />
      <Route exact path="/" component={Home} />
      <Route path="/fav" component={Home} />
    </main>
  </BrowserRouter>
);
```
### Handling 404 Requests
```
<Switch>
</Switch>
```
### Handling Redirects
```
<Redirect from='/home' to="/" />
```
### Add Links to Different Routes
```
<NavLink to="/" className="a b c" activeClassName="d e">
</NavLink>
```

Advanced type
```
import {PropTypes} from 'prop-types'
const HeaderLink = ({children, ...props})=>(
  <NavLink exact className='' {...props}>{children}</NavLink>
);
const Header=()=>( <HeaderLink to="/">Home</HeaderLink>)
HeaderLink.propTypes={
  children:PropTypes.node
}
```
