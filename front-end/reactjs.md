## Ref 활용하기

```jsx
import React from 'react'

class ChildComp extends React.Component {
  render() {
    return (
      <div ref={this.props.setRef}>Child</div>
    )
  }
}

class ParentComp extends React.Component {
  childRef = React.createRef()

  componentDidMount() {
    console.log(this.childRef.clientWidth)
    console.log(this.childRef.clientHeight)
  }

  this.setRef = ref => {
    this.childRef = ref
  }

  render() {
    return (
      <ChildComp setRef={this.setRef} />
    )
  }
}
```