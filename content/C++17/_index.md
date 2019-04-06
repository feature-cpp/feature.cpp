+++
author = "Sao Haruka"
date = "2019-03-11T00:30:00+09:00"
description = "description"
draft = false
tags = ["c++17"]
title = "C++17"
+++

# C++17の機能一覧

勉強会を開催した回をカッコ内に記載しています

## ```C++17``` 言語編

変数・データ構造関係

- 十六進浮動小数点数リテラル
- インライン変数 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- 構造化束縛 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- 波括弧初期化の型推論の新規則 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- [[maybe_unused]]属性 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- [[nodiscard]]属性 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- 値のコピー省略を保証 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- 厳密な式の評価順 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- 参照メンバをもつクラスの置き換え
- enum class変数の初期値として整数を指定する際の規則を調整

制御構文

- if文とswitch文の条件式と初期化を分離 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- [[fallthrough]]属性 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
-*範囲 for ループの制限緩和

ラムダ式

- ラムダ式での*thisのコピーキャプチャ ([vol.18](./summary/#nakameguro-feature-cpp-vol-18))

テンプレート

- 畳み込み式 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- テンプレートテンプレートパラメータにtypenameキーワードの使用を許可
- クラステンプレートのテンプレート引数推論 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- 非型テンプレートパラメータのauto宣言 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
-  全ての非型テンプレート引数の定数式評価を許可
-  変数テンプレートのデフォルトテンプレート引数を許可

定数式

- static_assertのメッセージ省略を許可 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- constexprラムダ ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- if constexpr文 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))

名前空間

- 入れ子名前空間の定義 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- 名前空間と列挙子への属性付加を許可 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- using宣言のパック展開

例外

- 例外仕様を型システムの一部にする ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- 非推奨だった古い例外仕様を削除 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))

属性

- [[fallthrough]]属性 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- [[maybe_unused]]属性 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- [[nodiscard]]属性 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- 名前空間と列挙子への属性付加を許可 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- 属性の名前空間指定に繰り返しをなくす ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- 不明な属性を無視する ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))

プリプロセッサ

- __has_include

機能の削除

- トライグラフの削除 ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- 非推奨だったregisterキーワードを削除
- 非推奨だったbool型に対するインクリメント演算子を削除
- 非推奨だった古い例外仕様を削除 ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))

小さな変更

- 更新された定義済みマクロ
- 機能テストマクロ
- noexcept付きのラムダ式から変換する関数ポインタにnoexceptを付加する
- UTF-8文字リテラル

その他

- std::*_v ([vol.4](./summary/#ebisu-feature-cpp-vol-4))
- over-aligned型対応new ([vol.4](./summary/#ebisu-feature-cpp-vol-4))


## ```C++17``` ライブラリ編


- Mathematical special functions
- Filesystem ([vol.15](./summary/#nakameguro-feature-cpp-vol-15)) 
- Parallelism ([vol.5](./summary/#ebisu-feature-cpp-vol-5))
- New algorithms  
(for_each_n, reduce, transform_reduce, exclusive_scan, inclusive_scan, transform_exclusive_scan, transform_inclusive_scan)
- New type: string_view (and basic_string_view) ([vol.14](./summary/#nakameguro-feature-cpp-vol-14)) 
- New type: any ([vol.10](./summary/#nakameguro-feature-cpp-vol-10))
- New class template: variant ([vol.11](./summary/#nakameguro-feature-cpp-vol-11))
- New class template: optional(vol.12/[vol.13](./summary/#nakameguro-feature-cpp-vol-13))
- invoke ([vol.16](./summary/#nakameguro-feature-cpp-vol-16))
- is_invocable, is_invocable_r, invoke_result ([vol.5](./summary/#ebisu-feature-cpp-vol-5))
- Elementary string conversions ([vol.18](./summary/#nakameguro-feature-cpp-vol-18))
- Alias template void_t ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- Alias template bool_constant ([vol.17](./summary/#nakameguro-feature-cpp-vol-17))
- Logical operation metafunctions ([vol.17](./summary/#nakameguro-feature-cpp-vol-17))
- Traits for SFINAE-friendly swap ([vol.17](./summary/#nakameguro-feature-cpp-vol-17))
- Trait is_aggregate ([vol.17](./summary/#nakameguro-feature-cpp-vol-17))
- Trait has_unique_object_representations
- as_const ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- Non-member size, data, empty
- clamp
- gcd and lcm
- Class shared_mutex ([vol.8](./summary/#nakameguro-feature-cpp-vol-8))
- Interference sizes (hardware_{con,de}structive_interference_size) ([vol.8](./summary/#nakameguro-feature-cpp-vol-8))
- Tuple apply ([vol.5](./summary/#ebisu-feature-cpp-vol-5))
- Construction from tuples
- Universal negator not_fn ([vol.5](./summary/#ebisu-feature-cpp-vol-5))
- Memory resources ([vol.9](./summary/#nakameguro-feature-cpp-vol-9))  
(synchronized_pool_resource, unsynchronized_pool_resource, monotonic_buffer_resource)
- A polymorphic allocator ([vol.9](./summary/#nakameguro-feature-cpp-vol-9))  
- A polymorphic allocator ([vol.9](./summary/#nakameguro-feature-cpp-vol-9))  
 std::pmr::vector&lt;T&gt; = std::vector&lt;T, polymorphic_allocator&lt;T&gt;&gt;
- Searcher functors ([vol.18](./summary/#nakameguro-feature-cpp-vol-18))

既存ライブラリが修正されたもの

- uncaught_exceptions() ([vol.6](./summary/#nakameguro-feature-cpp-vol-6))
- Improved insertion for unique-key maps ([vol.7](./summary/#nakameguro-feature-cpp-vol-7))
- Return type of emplace ([vol.18](./summary/#nakameguro-feature-cpp-vol-18))
- Splicing maps and sets ([vol.7](./summary/#nakameguro-feature-cpp-vol-7))
- Non-const string::data
- A variadic version of lock_guard called scoped_lock ([vol.8](./summary/#nakameguro-feature-cpp-vol-8))
- Variable templates for traits ([vol.17](./summary/#nakameguro-feature-cpp-vol-17))
- atomic::is_always_lock_free ([vol.8](./summary/#nakameguro-feature-cpp-vol-8))
- shared_ptr for arrays ([vol.13](./summary/#nakameguro-feature-cpp-vol-13))  
- shared_ptr::weak_type  ([vol.13](./summary/#nakameguro-feature-cpp-vol-13))  
- std::enable_shared_from_this ([vol.13](./summary/#nakameguro-feature-cpp-vol-13))  
- Three-dimensional hypotenuse
- Further uninitialized algorithms
- Incomplete type support for allocators
- Changes to &lt;chrono&gt;
- Constexpr for char_traits
- Improving pair and tuple
- Changes to common_type

Deprecate

- shared_ptr::unique ([vol.8](./summary/#nakameguro-feature-cpp-vol-8))

Temporarily discourage

 - memory_order_consume ([vol.8](./summary/#nakameguro-feature-cpp-vol-8))

その他

- C++ refers to C11
- Reserved namespaces
- C library synopses
- Term “forwarding reference”  
Term “default member initializer”  
Term “templated entity”  
Term “contiguous iterator”  
- Change “random number generator” to “random bit generator”
 
---

参考：
  
[https://cpprefjp.github.io/lang/cpp17.html](https://cpprefjp.github.io/lang/cpp17.html)  
[https://isocpp.org/files/papers/p0636r0.html](https://isocpp.org/files/papers/p0636r0.html)

