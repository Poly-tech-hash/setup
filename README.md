import React  from 'react';
import { BrowserRouter as Router, Switch, Route, Link } from "react-router-dom";
import Landing from './landing';
import Profile from './profile';
import About from './about';
import './index.css';

const App = () => {
    return (
        <>
        <Router>
            <div>
                <nav className="navigation">
                    <ul>
                        <li>
                            <Link to="/">Home</Link>
                        </li>
                        <li>
                            <Link to="/profile">Profile</Link>
                        </li>
                        <li>
                            <Link to="/about">About</Link>
                        </li>
                    </ul>
                </nav>

                <Switch>
                    <Route path="/profile">
                        <Profile/>
                    </Route>
                    <Route path="/about">
                        <About/>
                    </Route>
                    <Router path="/">
                        <Landing/>
                    </Router>
                </Switch>
            </div>
        </Router>
        </>
    )
}

export default App;    
