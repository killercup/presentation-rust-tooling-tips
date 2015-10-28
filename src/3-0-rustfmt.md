
## rustfmt

---

Auto­mat­i­cally refor­mat your Rust code to make it eas­ily parseable by humans

Get it from [github.com/nrc/rustfmt](https://github.com/nrc/rustfmt)

---

### The One True Rust Style?

<aside class="notes">

- Nothing is set in stone, RFCs need to be written to recommend any style.
- Rustfmt allows us to easily switch styles.

</aside>

---

### Current state

Good results, can be tweaked with some options.

----

#### Before

```plain
fn main() { return doughnutFryer.start() .then(|_| _frostingGlazer.start()) .then(|_| Future.wait([ _conveyorBelts.start(), sprinkleSprinkler.start(), sauceDripper.start() ])) .catchError(cannotGetConveyorBeltRunning) .then(|_| tellEveryoneDonutsAreJustAboutDone()) .then(|_| Future.wait([ croissantFactory.start(), _giantBakingOvens.start(), butterbutterer.start() ]) .catchError(_handleBakingFailures) .timeout(scriptLoadingTimeout, _handleBakingFailures) .catchError(cannotGetConveyorBeltRunning)) .catchError(cannotGetConveyorBeltRunning) .then(|_| { _logger.info("Let's eat!"); }); }
```

(From [nrc/rustfmt#296](https://github.com/nrc/rustfmt/issues/296))

---

#### After

```plain
fn main() {
    doughnutFryer.start()
                 .then(|_| _frostingGlazer.start())
                 .then(|_| {
                     Future.wait(_conveyorBelts.start(),
                                 sprinkleSprinkler.start(),
                                 sauceDripper.start())
                 })
                 .catchError(cannotGetConveyorBeltRunning)
                 .then(|_| tellEveryoneDonutsAreJustAboutDone())
                 .then(|_| {
                     Future.wait(croissantFactory.start(),
                                 _giantBakingOvens.start(),
                                 butterbutterer.start())
                           .catchError(_handleBakingFailures)
                           .timeout(scriptLoadingTimeout, _handleBakingFailures)
                           .catchError(cannotGetConveyorBeltRunning)
                 })
                 .catchError(cannotGetConveyorBeltRunning)
                 .then(|_| {
                     _logger.info("Let's eat!");
                 });
}
```

