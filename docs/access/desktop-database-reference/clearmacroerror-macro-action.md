---
title: ClearMacroError マクロ アクション
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296375"
---
# <a name="clearmacroerror-macro-action"></a>ClearMacroError マクロ アクション


**適用先:** Access 2013、Office 2013


You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.

## <a name="setting"></a>Setting

"ClaerMacroError/マクロエラーのクリア" アクションには、引数はありません。

## <a name="remarks"></a>注釈

- マクロでエラーが発生すると、エラーに関する情報が **MacroError** オブジェクトに格納されます。 " **[OnError](onerror-macro-action.md)** /エラー時" アクションを使用してエラーメッセージが表示されないようにしていない場合は、マクロが停止し、エラー情報が標準的なエラーメッセージに表示されます。 ただし、" **OnError** /エラー時" アクションを使用してエラーメッセージが表示されないようにした場合は、 **MacroError**オブジェクトに格納されている情報を条件またはカスタムエラーメッセージで使用することをお勧めします。
    
  After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.

- The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.

- **MacroError** オブジェクトには、一度に 1 つのエラー情報のみが格納されます。マクロで複数のエラーが発生した場合は、最後のエラーに関する情報だけが **MacroError** オブジェクトに格納されます。

- To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.

## <a name="example"></a>例

The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form. For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record. 条件** \[MacroError\]。\[0\]\<\>を指定**すると、 **MacroError**オブジェクトがテストされます。 If an error has occurred, the error number is non-zero, and the **MessageBox** action runs. The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed. Finally, running the **ClearMacroError** action clears the **MacroError** object.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>条件</p></th>
<th><p>アクション</p></th>
<th><p>引数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>[次へ] に移動し</strong>ます。 <strong></strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: カテゴリフォーム<strong>ビュー</strong>: <strong>formwindow Mode</strong>: <strong>Normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>オブジェクトの種類</strong>: <strong>formoboffname</strong>: カテゴリフォーム<strong>レコード</strong>: 以前</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]。件数&lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].件数&amp; &quot; [ &quot; MacroError] &amp;ActionName&amp; &quot;アクション。&quot;<strong>警告音</strong>: <strong>yestype</strong>: 情報</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

