# 何したか

- 改めて、Reactの基礎を復習するために環境構築。
- ポートフォリオを作成することに決定。
- 軽くHeader作成
- map関数の理解

# 理解した事
- lucide-reactの読み方「ルシーダリアクト」らしい。今まで間違えてた。
- map関数やる事は分かってるけど理解がきちんとできないのを以下の通り学習した。

## 個人的map()関数についての認識
以下のコードを参考
-  もともとあるnavLinks配列を1つずつ処理していく。
-  それをほかの要素（aタグとか）を含めた状態の配列をlinkという変数に格納している。
-  navLinks.map（　=> （））　これに（link）を追加している。

``` TypeScript
const navLinks = [
  { href: '#', label: 'About' },
  { href: '#', label: 'Portfolio' },
  { href: '#', label: 'Social' },
];

const Header = () => {
  return (
    <>
      {navLinks.map((link) => (
        <a key={link.href} href={link.href} className='text-sm font-semibold hover:text-primary'>
          {link.label}
        </a>
      ))}
    </>
  );
};

```

# 感想
- 確実に環境構築の速度が上がってきてナレッジも溜まってきた。
- vite, tailwind, shadcn/ui の流れマスターした。
- JavaScriptの基礎で迷ったり悩んだりすることがあるのが課題と感じた。特に三項演算子や関数の書き方や特徴。
