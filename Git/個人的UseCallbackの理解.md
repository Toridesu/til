# UseCallbackについて

## なぜ必要なの？
UseCallbackを使うと再レンダリングがされない！
以下のは使わない例
  
``` javascript
function MyComponent() {
  // このhandleClickは再レンダリングのたびに新しく作られる
  const handleClick = () => {
    console.log('クリックされました');
  };
  
  return <button onClick={handleClick}>クリックしてね</button>;
}
```

## useCallback の使い方

``` javascript
const 記憶したい関数 = useCallback(
  () => {
    // 実行したい処理
  },
  [依存する値1, 依存する値2, ...]
);
第2引数の配列（依存配列）は重要です：
```

この配列の中の値が変わったときだけ、関数が新しく作り直される
空の配列 [] を渡すと、その関数は初回レンダリング時に1回だけ作られ、その後は同じ関数が使われる

### 依存する値を使用する例

```
  const incrementWithCallback = useCallback(() => {
    setCount(count + 1);
  }, [count]);
```
  
