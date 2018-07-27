---
title: 下位互換機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- バージョン互換性 [excel 2007],XLL 互換性 [Excel 2007],下位互換性 [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798771"
---
# <a name="backward-compatibility"></a>下位互換機能

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
このトピックでは、Microsoft Excel の各バージョンにおける XLL 互換性の問題について説明します。
  
## <a name="useful-constant-definitions"></a>便利な定数の定義

XLL プロジェクト コードに、次に示すような定義を組み込んで、このコンテキストで使用されるすべてのリテラルによる数値のインスタンスを置き換えることを検討してください。これにより、バージョン固有のコードが明確になり、バージョンに関連する一見無害な形の数値によるバグが発生する可能性を抑えられるようになります。
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a>実行中のバージョンの取得

実行中のバージョンは、`Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` を使用して検出します。この `arg` は 2 に設定された数値型の **XLOPER** です。また、version は文字列型の **XLOPER** であり、後から強制的に整数に変換できます。 Microsoft Excel 2013 では、これは 15.0 です。 この操作には、[xlAutoOpen](xlautoopen.md) 関数を使用する必要があります。 その後、グローバル変数を設定することで、どのバージョンの Excel を実行しているかについて、プロジェクトに含まれるすべてのモジュールに通知できます。 これにより、コード内で **Excel12** と **XLOPER12** を使用する C API を呼び出すか、**Excel4** と **XLOPER** を使用する C API を呼び出すかを決定します。
  
C API のバージョンを検出するために **XLCallVer** を呼び出すことができますが、この方法では、Excel 2007 より前のどのバージョンを実行しているかについては示されません。 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>デュアル インターフェイスをエクスポートするアドインの作成

1 つの文字列を受け取り、ワークシートのデータ型のいずれかになる 1 つの値を返す XLL 関数について考えてみましょう。"PD" 型として登録され、次に示すようにプロトタイプされた関数をエクスポートできます。文字列は、長さカウント付きバイト文字列として渡されています。
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
これは完璧に動作しますが、いくつかの理由から、Excel 2007 以降のコードに対する理想的なインターフェイスにはなりません。
  
- C API のバイト文字列に関する制限が課せられ、Excel 2007 以降でサポートされる長い Unicode 文字列にアクセスできません。
    
- Excel 2007 以降の Excel は、**XLOPER** の受け渡しが可能です。ただし、これは内部で **XLOPER12** に変換されるため、Excel 2007 以降では、以前の Excel のバージョンのコードで実行する場合には存在しない暗黙的な変換のオーバーヘッドが発生します。
    
- この関数はスレッド セーフにされている可能性がありますが、型文字列が `PD$` に変更されると、Excel 2007 以降では登録に失敗します。
    
これらの理由から、Excel 2007 以降では `QD%$` として登録されていたユーザーに対して、コードがスレッド セーフであると想定して、次のようにプロトタイプされた関数をエクスポートする必要があります。
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Excel 2007 以降では別の関数を登録することが望ましいもう 1 つの理由は、XLL 関数が最大 255 個の引数を受け入れる (以前のバージョンでは 30 個に制限されていました)。
  
好都合なことに、プロジェクトから両方のバージョンをエクスポートすると、両方のメリットが得られます。その後、実行中の Excel バージョンを検出して、最適な関数を条件によって登録します。詳細と実装例については、「[Excel 2007 のアドイン (XLL) の開発](http://msdn.microsoft.com/ja-JP/library/aa730920.aspx)」を参照してください。
  
このアプローチでは、同じワークシートを Excel 2003 で実行した場合と、Excel 2007 以降で実行した場合では、異なる結果が表示される可能性があります。たとえば、Excel 2003 では Excel 2003 ワークシート セル内の Unicode 文字列を ASCII バイト文字列にマッピングし、その文字列を切り詰めてから XLL 関数に渡します。Excel 2007 以降の Excel では、適切な方法で登録された XLL 関数に、変換されていない Unicode 文字列を渡します。これが、異なる結果の原因になります。このような可能性とユーザーへの影響に対する注意は、アップグレード時以外にも必要になります。たとえば、いくつかの組み込みの数値関数は、Excel 2000 と Excel 2003 との間で改善されています。
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>新しいワークシート関数と分析ツール関数

分析ツール (ATP) 関数は、Excel 2007 以降の Excel に含まれています。 以前は、XLL では [xlUDF](xludf.md) を使用することでのみ ATP 関数を呼び出せました。 Excel 2007 以降では、xlcall.h で定義されている関数の列挙値を使用して、ATP 関数を呼び出す必要があります。 「DLL からのユーザー定義関数の呼び出し」の例では、2 通りの方法を示しています。
  
## <a name="see-also"></a>関連項目

- [C API コールバック関数 Excel4、Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Excel での C API を使用したプログラミング](programming-with-the-c-api-in-excel.md)
- [Excel 用 C API の新機能](what-s-new-in-the-c-api-for-excel.md)

