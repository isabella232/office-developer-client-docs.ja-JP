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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308471"
---
# <a name="submacro-macro-statement"></a>Submacro マクロ ステートメント

**適用先:** Access 2013、Office 2013

**Submacro**ステートメントは、マクロデザイナーウィンドウで別のマクロを定義します。

## <a name="setting"></a>Setting

Submacro アクションの引数は次のとおりです。

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

次のマクロは、"OnError/**エラー**時" アクションの使用方法を示します。 この例では、" **OnError** /エラー時" アクションは、エラーが発生したときに ErrorHandler という名前のカスタムエラー処理マクロを実行するように指定します。 エラーが発生すると、CatchErrors submacro が呼び出されます。 エラー番号が2102の場合は、特定のメッセージが表示され、マクロの実行が停止します。 それ以外の場合は、エラーを説明するメッセージが表示され、マクロが一時停止して、追加のトラブルシューティングを実行できるようになります。 ErrorHandler マクロは、 **MacroError**オブジェクトを参照するメッセージボックスを表示して、エラーに関する情報を表示します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

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
