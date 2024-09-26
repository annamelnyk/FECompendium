# Intro in RxJS & Reactive Programming

## Basic terms

<ul>
  <li>Reactive Programming:
    <ul>
      <li>Programming paradigm that works with **asyncronous data streams**</li>
      <li>Data streams can be created from:<br>
        - UI Events<br>
        - HTTP Requests<br>
        - File Systems<br>
        - Array like objects<br>
        - Memory / Cache<br>
      </li>
      <li>**Stream**:<br>
        - A sequance of ongoing events ordered in time <br>
        - Emits a **value**, **error** and complete **signal** - 3 values we can get from stream<br>
      </li>
      <li>**Observables:**<br>
        - are used to watch these streams and emit functions when a value, error or completed signal returned <br>
        - can be subscribed to by an observer<br>
        - will constantly watch streams and will upate accordingly <br>
        - we can interact with data streams as any regular array<br>
      </li>
      <li>**Reactive Extensions / Reactive X (RxJS)** by Microsoft<br>
        - A library for composing asyncronous programs by using observable sequences<br>
        - Provides a list of operators which allow us to filter, select, transform, combine and compose observables<br>
      </li>
      <li></li>
      <li></li>
    </ul>
  </li>
</ul>
