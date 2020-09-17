### render() block in React
#####  In Render block we have two types of method 
  - {this.methodName()}
  - {this.methodName}

####  - {this.methodName()}
  - This is type expression we use when we load data statically at the time of render block invoing like: className 

  example: 
  
  
  ```
  renderTags = () => {
    if (this.state.tags.length === 0) return <p>No tags Found</p>;
    return (
      <ul>
        {this.state.tags.map((i, tag) => (
          <li key={i}>{tag}</li>
        ))}
      </ul>
    );
  };
   getBadgeClasses() {
    let classes = "badge m-2 badge-";
    classes += this.state.count === 0 ? "warning" : "primary";
    return classes;
  }

  formatCount() {
    const { count } = this.state;
    return count === 0 ? "Zero" : count;
  }

   render() {
    return (
      <div>
        <span className={this.getBadgeClasses()}>{this.formatCount()}</span>
        {this.state.tags.length === 0 && "Pelase docr"}
        <ul>{this.renderTags()}</ul>
      </div>
    );
  }
  ```
####   {this.methodName} - HandleEvent

- This type of method use when we want to change state variable value (setState({})). In this type only we have to write the name of the method (not calling) with dom event.
- This is called function or method calll by reference.



```
 handleIncrement() {
    this.setState({ count: ++this.state.count });
  }
render() {
    return (
      <div>
        <button
          onClick={this.handleIncrement}
          className="btn btn-secondary btn-sm"
        >
          Increment
        </button>
      </div>
    );
  }
```

#####  - Problem of function/method ref :
  - You can not pass argumnet 
  Let us solve this by two function/method
```

  handleIncrement = (product) => {
    console.log(product);
    this.setState({ count: ++this.state.count });
  };
  doHandleIncrement = () => {
    this.handleIncrement({ id: 1 });
  };
  
 render() {
    return (
      <div>
        <button
          onClick={this.doHandleIncrement}
          className="btn btn-secondary btn-sm" >
          Increment
        </button>
      </div>
    );
  }


``` 
 - As you can see here we write extra hoHandleIncrement method (helper mehtod) to pass an argument to handleIncrement(product);
 - But this is approach is not so good.
 - To Overcome this Problem we can write a inline function 
 
```
  handleIncrement = (product) => {
      console.log(product);
      this.setState({ count: ++this.state.count });
    };

    render() {
      return (
        <div>
          <button
            onClick={() => this.handleIncrement({ id: 1 })}
            className="btn btn-secondary btn-sm" >
            Increment
          </button>
        </div>
      );
    }
    
    
    
    
    or 
     <button
            onClick={() => this.handleIncrement(product)}
            className="btn btn-secondary btn-sm" >
            Increment
    </button>
````



