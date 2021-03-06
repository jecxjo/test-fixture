# 0.5.1.0 (October 30, 2017)

  - Added lifting instances for `MonadIO`, `MonadThrow`, `MonadCatch`, and `MonadMask` to `TestFixtureT`.

# 0.5.0.2 (July 27, 2017)

  - Added support for `template-haskell-2.12.0.0` and GHC 8.2.1.

# 0.5.0.1 (June 2, 2017)

  - Fixed an issue where using `mkFixture` with a typeclass that used the `DefaultSignatures` extension caused an internal error ([#30](https://github.com/cjdev/test-fixture/issues/30)).

# 0.5.0.0 (November 28, 2016)

  - **Breaking**: `mkFixture` now supports constraints in the same form as a Haskell `deriving` clause, which permits “partially-applied” constraints. A new `ts` quasiquoter is provided for the purpose of writing a comma-separated list of Haskell types; see the documentation for more details ([#25](https://github.com/cjdev/test-fixture/issues/25)).
  - Generating fixtures that do not derive any typeclasses no longer produces an error ([#28](https://github.com/cjdev/test-fixture/issues/28)).

# 0.4.2.0 (November 14, 2016)

  - Attempting to generate a fixture for a multi-parameter typeclass now produces a better error message ([#24](https://github.com/cjdev/test-fixture/issues/24)).
  - Fixtures can now be generated for typeclasses containing infix operators as methods. They will be prefixed with a tilde (`~`) instead of an underscore ([#26](https://github.com/cjdev/test-fixture/issues/26)).
