---
title: パラメトリック検定とノンパラメトリック検定
tags: [note, study, statistics]
---

## 概要
- [仮設検定](note/study/statistics/hypothesis-test.md)におけるパラメトリック検定とは，母集団のサンプルに対する検定のうち，母集団の分布を事前に仮定する検定である
- 母集団のサンプルに対する検定のうち，パラメトリック検定でないものはノンパラメトリック検定である

## パラメトリック検定
- 母集団がある特定の分布であると事前に仮定する検定
	- ノンパラメトリック検定に比べて，計算が楽
		- 手計算はこっちの方が嬉しい
	- 母集団が仮定と異なる分布を持つ場合，検定の結論に意味は無い
- 事前検定で母集団の仮定を検証するのはやめた方がいい（後述）

## ノンパラメトリック検定
- 母集団の分布を仮定しない検定
	- 計算がめんどくさい
		- サンプルサイズが頭おかしいほど大きくない限り，コンピュータなら一瞬
	- 仮定に沿うパラメトリック検定が存在する場合，それよりも精度は落ちるが，実用的な問題はない

## 事前検定
- 欲しい結果を得る検定の前に行われる検定のこと
	- [多重検定](note/study/statistics/hypothesis-test-multiplicity.md)の問題を孕む
		- 個人的には，大抵の場合において事前検定は愚行だと思っている
- 母集団の正規性を仮定するパラメトリック検定を使いたいがために，事前検定として正規性の検定(Shapiro-wilk test)をする人がいる
	- 個人的には多重検定問題沼に足を突っ込むぐらいなら，そこまでしてパラメトリック検定を使う必要はないと思う
	- 大人しくノンパラメトリック検定を使うべき
	- そもそもコンピュータ使えば計算コストは無視できる

## まとめ
- 仮設検定は2つに分けられる
	- パラメトリック検定: 母集団の分布になんらかの仮定が必要な検定
	- ノンパラメトリック検定: それ以外の検定
- パラメトリック検定をしたいがために多重検定を使うぐらいならば，ノンパラメトリック検定を使うべき