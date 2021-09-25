---
title: Excel のコマンド、関数、および状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- states [excel 2007],commands [Excel 2007],worksheet functions [Excel 2007],macro-sheet functions [Excel 2007],Excel states
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: a26a1bd43c67f0fcb2b7f916db8ba3f7cb9b389f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601395"
---
# <a name="excel-commands-functions-and-states"></a>Excel のコマンド、関数、および状態

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel は、コマンドと関数という、2 種類の別々の追加機能を識別します。
  
## <a name="commands"></a>コマンド

Excel のコマンドには次のような特性があります。
  
- ユーザーが行うのと同じ方法でアクションを実行する。
    
- Excel の設定を変更する、ドキュメントを開く、閉じる、編集する、再計算を開始するなど、ユーザーが実行可能なあらゆる操作 (使用するインターフェイスの制限に依存します) を実行できる。
    
- トラップされた特定のイベントが発生したときに、呼び出されるようセットアップできる。
    
- ダイアログ ボックスを表示でき、ユーザーと対話できる。
    
- 左クリックなど、オブジェクト上でアクションが行われるときに呼び出されるように、オブジェクトの制御にリンクできる。
    
- 再計算中に Excel がコマンドを呼び出すことはない。
    
- 再計算中に関数がコマンドを呼び出すことはできない。
    
## <a name="functions"></a>関数

Excel の関数は、次のことを実行します。
  
- 通常、引数を受け取り、常に結果を返す。
    
- Excel の式の部分として、1 つ以上のセルに入力できる。
    
- 定義された名前定義で使用できる。
    
- 条件付き書式の制限およびしきい値の式で使用できる。
    
- コマンドで関数を呼び出せる。
    
- 関数がコマンドを呼び出すことはできない。
    
さらに Excel では、ユーザー定義ワークシート関数と、マクロ シート上で動作するよう設計されたユーザー定義関数とを区別しています。Excel では、ユーザー定義のマクロ シート関数がマクロ シートだけで使用されるように制限することはありません。これらの関数は、通常のワークシート関数を使用できる場所であればどこでも使用できます。
  
### <a name="worksheet-functions"></a>ワークシート関数

Excel ワークシート関数には、次の事項が当てはまります。
  
- マクロ シート情報関数にはアクセスできない。
    
- 計算されていないセルの値を取得できない。
    
- Excel 2007 以降では、スレッド セーフとして作成し、登録できる。
    
### <a name="macro-sheet-functions"></a>マクロシート関数

Excel マクロシート関数には、次の事項が当てはまります。
  
- マクロ シート情報関数にアクセスできる。
    
- 呼び出し元のセルの値を含む再計算されたセルの値を取得できる。
    
- Excel 2007 以降では、スレッド セーフとみなされない。
    
How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function. If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails. Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.
  
Excel は、Microsoft Visual Basic for Applications (VBA) の UDF をマクロ シート等価の関数として扱います。それらの UDF はワークスペース情報と計算されないセルの値にアクセスでき、Excel 2007 以降、スレッド セーフとはみなされません。
  
## <a name="excel-states"></a>Excel の状態

ユーザー、外部プロセス、マクロを実行するトラップされたイベント、または時間指定の Excel のハウスキーピング イベント (**Autosave** など) のアクションによって、Excel はどの時点でも、数ある状態のうちのどれか 1 つに入ります。
  
ユーザーは、次のような状態を経験します。
  
- **準備完了状態:** 実行中のコマンドやマクロはありません。表示しているダイアログ ボックスはありません。編集されているセルはなく、ユーザーは切り取り、コピー、貼り付けの操作の途中ではありません。フォーカスしている埋め込みオブジェクトはありません。 
    
- **編集モード:** ユーザーが、ロック解除されたセル、または保護されていないセルに、有効な入力文字を入力し始めた場合や、1 つ以上のロック解除されたセルまたは保護されていないセルで **F2** キーを押した場合です。 
    
- **切り取り、コピー、貼り付けモード:** ユーザーがセルまたはセル範囲を切り取ったりコピーしたりして、それをまだ貼り付けていない場合や、複数の貼り付け操作が可能な [形式を選択して貼り付け] ダイアログ ボックスを使用して貼り付けた場合です。 
    
- **ポイント モード:** ユーザーは、数式を編集中で、編集している数式にアドレスが追加されるセルを選択しているところです。 
    
ユーザーは、編集、ポイント、貼り付け、コピー モードを **[ESC]** キーを押すことによって解除でき、Excel は準備完了状態に戻ります。他のイベントでは、これらの状態を次のように解除することができます。 
  
- ユーザーがビルトイン ダイアログ ボックスを開く。
    
- ユーザーが再計算を開始する。
    
- ユーザーがコマンドを実行する。
    
- Excel が **Autosave** 操作を実行する。 
    
- タイマー イベントがトラップされる。
    
最後の例は、アドイン開発者にとって重要です。タイマー イベント トラップが頻繁に設定され実行されることが、Excel の通常の使いやすさに及ぼす影響を検討する必要があります。この点がアドインの機能性にとって重要な部分である場合、ユーザーが必要に応じて切り取り、コピー、貼り付けの操作を正常に行えるように、アドインの実行を一時的に中断する分かりやすい方法をユーザーに提供する必要があります。
  
## <a name="see-also"></a>関連項目



[Excel プログラミングの概念](excel-programming-concepts.md)
  
[時間のかかる操作でユーザーによる中断を許可する](permitting-user-breaks-in-lengthy-operations.md)

