## Styling input type: range

- Sample Code
```css
// Slider Thumb Styling
input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  border: 6px solid #6c6e70;
  height: 24px;
  width: 24px;
  border-radius: 12px;
  background: #303438;
  cursor: pointer;
  margin-top: -5px; /* You need to specify a margin in Chrome, but in Firefox and IE it is automatic */
}

/* All the same stuff for Firefox */
input[type="range"]::-moz-range-thumb {
  border: 6px solid #6c6e70;
  height: 12px;
  width: 12px;
  border-radius: 12px;
  background: #303438;
  cursor: pointer;
}

/* All the same stuff for IE */
input[type="range"]::-ms-thumb {
  border: 6px solid #6c6e70;
  height: 24px;
  width: 24px;
  border-radius: 12px;
  background: #303438;
  cursor: pointer;
}

// Slider Track Styling
input[type="range"] {
  -webkit-appearance: none; /* Hides the slider so that custom slider can be made */
  width: 100%; /* Specific width is required for Firefox. */
  background: transparent; /* Otherwise white in Chrome */
}

input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
}

input[type="range"]:focus {
  outline: none; /* Removes the blue border. You should probably do some kind of focus styling for accessibility reasons though. */
}

input[type="range"]::-ms-track {
  width: 100%;
  cursor: pointer;

  /* Hides the slider so custom styles can be added */
  background: transparent;
  border-color: transparent;
  color: transparent;
}

input[type="range"]::-webkit-slider-runnable-track {
  width: 100%;
  height: 15px;
  cursor: pointer;
  background: #454547;
  border-radius: 4px;
}

input[type="range"]:focus::-webkit-slider-runnable-track {
  background: #454547;
}

input[type="range"]::-moz-range-track {
  width: 100%;
  height: 15px;
  cursor: pointer;
  background: #454547;
  border-radius: 4px;
}

input[type="range"]::-ms-track {
  width: 100%;
  height: 15px;
  cursor: pointer;
  background: transparent;
  border-color: transparent;
  border-width: 16px 0;
  color: transparent;
}
input[type="range"]::-ms-fill-lower {
  background: #454547;
  border-radius: 4px;
}
input[type="range"]:focus::-ms-fill-lower {
  background: #454547;
}
input[type="range"]::-ms-fill-upper {
  background: #454547;
  border-radius: 4px;
}
input[type="range"]:focus::-ms-fill-upper {
  background: #454547;
}
```