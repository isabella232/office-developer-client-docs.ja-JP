---
title: StopMacro マクロ アクション
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308499"
---
# <a name="stopmacro-macro-action"></a>StopMacro マクロ アクション

**適用先:** Access 2013、Office 2013

**StopMacro** アクションを使用して、現在実行中のマクロを中止できます。

## <a name="setting"></a>Setting

**StopMacro** アクションには引数はありません。

## <a name="remarks"></a>注釈

通常、このアクションは、マクロを中止する必要が生じた場合に使用します。このアクションが定義されているマクロ内のアクション行に条件式を指定できます。条件式の評価が **True** (-1) の場合、Microsoft Access はマクロを中止します。

たとえば、カスタム ダイアログ ボックスに入力された日付の注文の合計が表示されるフォームを開くマクロを作成するとします。条件式を使用すると、ダイアログ ボックスの [ **注文日**] コントロールの日付が必ず有効になるように指定できます。有効でない場合は、" **MessageBox/メッセージボックス** " アクションによってエラー メッセージを表示し、" **StopMacro/マクロの中止** " アクションでマクロを中止することができます。

マクロ内で " **Echo/エコー** " アクションや " **SetWarnings/メッセージの設定** " アクションを使用して、エコーまたはシステム メッセージの表示がオフになっている場合は、" **StopMacros/マクロの中止** " アクションを実行すると、これらの設定が自動的にオンに戻ります。

このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。

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
