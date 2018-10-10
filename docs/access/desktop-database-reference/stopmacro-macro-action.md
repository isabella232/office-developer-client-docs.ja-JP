---
title: StopMacro マクロ アクション
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a918fd128456450c21b5a36e74b7266df661cb75
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477919"
---
# <a name="stopmacro-macro-action"></a>StopMacro マクロ アクション

**適用されます**Access 2013 |。Office 2013

" **StopMacro/マクロの中止** " アクションを使用すると、現在実行中のマクロを中止できます。

## <a name="setting"></a>設定

" **StopMacro/マクロの中止** " アクションには、引数はありません。

## <a name="remarks"></a>注釈

通常、このアクションは、マクロを中止する必要が生じた場合に使用します。 このアクションが定義されているマクロ内のアクション行に条件式を指定できます。 式は、 **True** (-1) に評価されると、Microsoft Access はマクロを停止します。

たとえば、カスタム ダイアログ ボックスに入力された日付の注文の合計が表示されるフォームを開くマクロを作成するとします。条件式を使用すると、ダイアログ ボックスの [ **注文日**] コントロールの日付が必ず有効になるように指定できます。有効でない場合は、" **MessageBox/メッセージボックス** " アクションによってエラー メッセージを表示し、" **StopMacro/マクロの中止** " アクションでマクロを中止することができます。

マクロ内で " **Echo/エコー** " アクションや " **SetWarnings/メッセージの設定** " アクションを使用して、エコーまたはシステム メッセージの表示がオフになっている場合は、" **StopMacros/マクロの中止** " アクションを実行すると、これらの設定が自動的にオンに戻ります。

このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。

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
