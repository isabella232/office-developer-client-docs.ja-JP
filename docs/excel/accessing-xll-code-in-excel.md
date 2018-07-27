---
title: Excel での XLL コードへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accessing xll code [excel 2007],XLLs [Excel 2007], accessing code,commands [Excel 2007], registration,functions [Excel 2007], registration,calling XLLs from Excel,registering commands [Excel 2007],registering functions [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798768"
---
# <a name="accessing-xll-code-in-excel"></a>Excel での XLL コードへのアクセス

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
XLL に含まれる関数やコマンドに Microsoft Excel でアクセスできるようにするには、次の事柄が必要となります。
  
- XLL によってエクスポートされなければなりません。
    
- Excel に登録する必要があります。
    
## <a name="registering-functions-and-commands-with-excel"></a>関数とコマンドを Excel に登録する

登録することによって、DLL エントリ ポイントについて次のことを Excel に指示します。
  
- 非表示かどうか。また関数の場合には、関数ウィザードに表示するかどうか。
    
- XLM マクロシートからのみ呼び出せるか、あるいはワークシートからも呼び出せるか。
    
- コマンドの場合、ワークシート関数か、またはマクロシート同等関数かどうか。
    
- XLL/DLL エクスポート名、および Excel で使用する名前。
    
- 関数の場合:
    
  - 返すデータ型、および引数として取るデータ型。
    
  - 引数をインプレースで変更して結果を返すかどうか。
    
  - 揮発性かどうか。
    
  - スレッド セーフであるかどうか (Excel 2007 以降でサポートされています)。
    
  - 関数貼り付けウィザードとオートコンプリート エディターに、関数の呼び出しを支援するために表示するテキスト。
    
  - リスト表示に使用する関数カテゴリ。
    
前述の点は、すべて C API 関数の [xlfRegister](xlfregister-form-1.md) を使用して行えます。この関数は XLM 関数の **REGISTER** に相当します。
  
## <a name="calling-xll-functions-directly-from-excel"></a>Excel から直接 XLL 関数を呼び出す

XLL ワークシート関数とマクロシート関数を登録すると、組み込み関数を呼び出すことが可能な次に示すすべての場所からそれらも呼び出せます。
  
- ワークシートの単一セルまたは配列数式。
    
- マクロシートの単一セルまたは配列数式。
    
- 定義された名前の定義。
    
- 条件付き書式のダイアログ ボックスの、条件と制限のフィールド。
    
- C API 関数 [xlUDF](xludf.md) を介して他のアドインから。
    
- **Application.Run** メソッドを介して Visual Basic for Applications (VBA) から。 
    
C API 関数 **xlfCaller** を使用すると、関数内の呼び出し元セルへの参照またはセルの範囲を取得できます。関数がセルの条件付き書式の式から呼び出された場合、関連する 1 つまたは複数のセルへの参照が返されます。したがって、セルの数式に XLL 関数が含まれているとは限りません。関数が VBA ユーザー定義関数 (UDF) から呼び出された場合、**xlfCaller** は VBA 関数を呼び出したセルのアドレスを再び返します。詳細については、「[xlfCaller](xlfcaller.md)」を参照してください。
  
> [!NOTE]
> また Excel は、[**関数貼り付けウィザード**] および [**置換**] ダイアログ ボックスから XLL 関数コードを呼び出します。 **[関数引数貼り付け]** ダイアログ ボックスではコードの通常の実行を制限する必要がある場合があります。特に、関数の実行に長時間かかる可能性がある場合にはそう言えます。 関数がこれらのいずれかのダイアログ ボックスから呼び出されているかどうかを調べるには、そのいずれかが前面のウィンドウであるかどうか、前面のウィンドウであればそのどれであるかを判別するコードを、すべての開いているウィンドウで繰り返して、プロジェクト内で実装する必要があります。 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Excel から直接 XLL コマンドを呼び出す

XLL コマンドを登録すると、他のユーザー定義マクロを呼び出すことができる次に示すあらゆる方法で XLL コマンドを呼び出すことができます。
  
- ワークシートに埋め込まれているコントロール オブジェクトに関連付けることによって。
    
- [マクロの実行] ダイアログ ボックスから。
    
- **Application.Run** メソッドを使用して VBA ユーザー定義マクロから。 
    
- カスタマイズされたメニュー項目またはツールバーから。
    
- コマンドを登録するときにセットアップされるショートカット キーボード操作を使用して。
    
- 指定したイベントがトラップされるときに実行するコマンドとして。
    
> [!NOTE]
> XLL コマンドは非表示で、Excel のダイアログ ボックスで使用できるマクロの一覧に表示されません。ただし、[マクロ名] フィールドに手動で入力できます。Excel では、それらのダイアログ ボックスで、DLL エクスポート名ではなく登録されたとおりの名前であることが必要となります。 
  
Excel に登録されているすべての XLL コマンドは、次の形式であることが Excel で想定されています。
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

Excel は戻り値を無視します。ただし、XLM マクロ シートから呼び出されたものを除きます (この場合、戻り値は **TRUE** または **FALSE** に変換されます)。そのため、コマンドが正常に実行された場合は 1 を返す必要があります。また、コマンドが失敗したり、ユーザーによって取り消されたりした場合は 0 を返す必要があります。
  
C API 関数の **xlfCaller** を使用すると、コマンドが呼び出された方法についての情報を取得できます。詳細については、「[xlfCaller](xlfcaller.md)」を参照してください。
  
Excel 2007 以降のユーザー インターフェイスは以前のバージョンのものとは大きく異なります。ほとんどの場合、カスタム メニュー バー、メニュー、サブメニュー、メニュー項目、ユーザー設定ツールバー、ツールバー ボタンの追加と削除を行える C API 関数が引き続きサポートされています。ただし、必ずしも、ユーザーがこれまでに慣れている方法で追加項目が使用可能になるわけではありません。追加機能が引き続き利用できるかどうかを注意して確認し、利用できない場合にはバージョン固有のカスタマイズを実装してください。Excel 2007 以降、ユーザー インターフェイスはマネージ コード モジュールを使用して最適の方法でカスタマイズされていて、XLL コマンドと密に連動させることができます。
  
## <a name="see-also"></a>関連項目

- [XLL を作成する](creating-xlls.md)
- [関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)
- [Excel XLL の開発](developing-excel-xlls.md)



