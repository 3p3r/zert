# zert

"zert" polyglot runtime for ops workflows.

## mvp

```zert

# This is a TOML-like source

[zert]
version = "0.0.0"
persist = true

[definitions]
<?js
  let n = 0;
  function add_one() {
    n += 1;
    return n;
  }
?>

[reuse]
<?js
  // blah ...
  // blah ...
  // blah ...
  const boo = "<?js add_one() ?>";
  console.log(boo);
  <?py
    # blah ...
    # blah ...
    # blah ...
    foo = "<?js add_one() ?>"
    print(foo)
  ?>
?>

```
