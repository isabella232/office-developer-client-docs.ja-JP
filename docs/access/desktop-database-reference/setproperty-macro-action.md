---
title: SetProperty マクロ アクション
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314575"
---
# <a name="setproperty-macro-action"></a>SetProperty マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **SetProperty** action to set a property for a control on a form or a report.

## <a name="setting"></a>Setting

"SetProperty/プロパティの設定" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>コントロール名</p></td>
<td><p>プロパティ値を設定する対象のフィールドまたはコントロールの名前を入力します。 完全な構文ではなく、コントロール名のみを指定してください。 カレント フォームまたはカレント レポートのプロパティを設定する場合は、この引数を指定しないでください。</p></td>
</tr>
<tr class="even">
<td><p>プロパティ</p></td>
<td><p>設定するプロパティを選択します。このアクションを使用して設定できるプロパティの一覧については、この記事の「解説」セクションを参照してください。</p></td>
</tr>
<tr class="odd">
<td><p>値</p></td>
<td><p>プロパティに対して設定する値を入力します。値が [はい] または [いいえ] のどちらかになるプロパティでは、[はい] の場合は「-1」、[いいえ] の場合は「0」を入力します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- "SetProperty/プロパティの設定" アクションを使用すると、コントロールの "Enabled/使用可能"、"Visible/可視"、"Locked/ロック"、"Left/左"、"Top/上"、"Width/幅"、"Height/高さ"、"Fore Color/前景色"、"Back Color/背景色"、または "Caption/標題" の各プロパティを設定できます。

- " ***value/値***" 引数に無効な値を入力すると、エラーは発生しませんが、引数がどのように解釈されるかに応じて、プロパティは別の値に変更される可能性があります。

- You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property. If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it. If the form or report is already open, you can use the **SelectObject** action to select it. You can then use the **SetProperty** action to set the property. Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.

- To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.

## <a name="example"></a>例

次の例は、"SetProperty/プロパティの設定" アクションを使用して、 **MyTextBox**テキストボックスの表示/非表示を切り替える方法を示しています。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
