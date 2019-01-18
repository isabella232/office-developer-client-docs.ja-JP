---
title: Submacro マクロ ステートメント
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caabfb0f4e90134c10d5ab728f19e1fd2a4437dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716195"
---
# <a name="submacro-macro-statement"></a>Submacro マクロ ステートメント

**適用されます**Access 2013、Office 2013。

**サブマクロ**ステートメントは、マクロ デザイナー ウィンドウで、別のマクロを定義します。

## <a name="setting"></a>設定

**サブマクロ**のアクションには、次の引数があります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>名前</p></td>
<td><p>はい</p></td>
<td><p>マクロの名前として表示する文字列。</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>例

次のマクロは、" **OnError/エラー時** " アクションの使用例を示しています。この例では、エラーが発生したときに Access が " **ErrorHandler**" という名前のカスタム エラー処理マクロを実行するように、" OnError/エラー時 " アクションが指定されています。エラーが発生すると、 CatchErrors サブマクロが呼び出されます。エラー番号が 2102 の場合、特定のメッセージが表示され、マクロの実行が停止します。それ以外の場合は、エラーの内容を説明するメッセージが表示され、マクロが一時停止します。したがって、追加のトラブルシューティングを行うことができます。 ErrorHandler マクロは、 **MacroError** オブジェクトを参照するメッセージ ボックスを表示して、エラーに関する情報を表示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
