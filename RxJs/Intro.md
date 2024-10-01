# Intro in RxJS & Reactive Programming

## Basic terms

<ul>
  <li>Reactive Programming:
    <ul>
      <li>Programming paradigm that works with **asyncronous data streams**</li>
      <li>It is a declarative programming paradigm conserned with data streams and propagation of change</li>
      <li>Code is reactive when an input leads to an automatic change of output</li>
      <li>Reactive development let us to:
      - react to user actions<br>
      - react to state chages <br>
      - combine data streams<br>
      - communicate between data components<br>
      - be resilient to errors<br>
      - manage state<br>
      </li>
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
        - By documentation **RxJS** is a library for composing asyncronous and event-based programs by using observable sequences<br>
        - A library for observing and reacting to data and events by using observable sequences<br>
        - A library for composing asyncronous programs by using observable sequences<br>
        - Provides a list of operators which allow us to filter, select, transform, combine and compose observables<br>
      </li>
      <li>**Why RxJs instead of:**<br>
        - **Callback (is a functions that can be called back after async operation is complete):** - but is hard to manage with nested async operations<br>
        - **Promise (is an object that may produce a single value in a future):** - but it can handle only single emittion and it is not cancellable<br>
        - **async/await (is a special syntax that allows to write async code that looks syncronous):** - but it also can handle only single emittion and it is not cancellable)<br>
        **Why RxJs:**<br>
          <ul>
            <li>Allow to work with different data sources using same techniques  and operators</li>
            <li>**Compositionsl**. Allow easily combile and compose data from different sources</li>
            <li>**Watchful**. Can producde multiple values over time and uses push model that notifies our code when specific action occured</li>
            <li>**Lazy**. Evoluation will not start until subscription. It will execute only when we need a result</li>
            <li>**Haddle errors**</li>
            <li>**Cancellable**</li>
          </ul>
      </li>
      <li>**How is RxJs used in Angular**<br>
        - In Routing (this.route.params, this.route.data, this.route.events)<br>
        - In Reactive Forms<br>
        - HttpClient<br>
      </li>
      <li>**Observer**:<br>
      - is a collection of callbacks that knows how listen to values deliveresd by the Observable<br>
      - an Observer is a consumer of values delivered by an Observable<br>
      - an Observer is also defined as an interface with *next*, *error* and *complete* methods<br>
      - **Subscriber** - the subclass which implements Observer interface<br>
      **Subscriber** - is an Observer that can unsubscribe from an Ob servable<br>
      **Observer** - observes and responds to notifications<br>
      **Observable** - a collection of events or values emitted over time. Events come from: user actions, application events, response from http, internal structures<br>
      - **Hot Observable** - emits values right away
      - **Cold Observable** - does not emit values untill there is the subscriber

      </li>
    </ul>
  </li>
</ul>
