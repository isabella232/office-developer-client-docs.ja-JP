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
ms.localizationpriority: medium
ms.openlocfilehash: 675b8926d69b7cb5f52ed299d85d05dcd9cd82b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553208"
---
# <a name="clearmacroerror-macro-action"></a>ClearMacroError マクロ アクション


**適用先:** Access 2013、Office 2013


You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.

## <a name="setting"></a>設定

"ClaerMacroError/マクロエラーのクリア" アクションには、引数はありません。

## <a name="remarks"></a>注釈

- マクロでエラーが発生すると、エラーに関する情報が **MacroError** オブジェクトに格納されます。 OnError アクションを使用 **[](onerror-macro-action.md)** してエラー メッセージを抑制していない場合、マクロは停止し、エラー情報は標準のエラー メッセージに表示されます。 ただし **、OnError** アクションを使用してエラー メッセージを抑制した場合は、条件またはカスタム エラー メッセージで **MacroError** オブジェクトに格納されている情報を使用できます。
    
  After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.

- The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.

- **MacroError** オブジェクトには、一度に 1 つのエラー情報のみが格納されます。マクロで複数のエラーが発生した場合は、最後のエラーに関する情報だけが **MacroError** オブジェクトに格納されます。

- To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.

## <a name="example"></a>例

The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form. For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record. 条件 **\[ MacroError \] . \[数値 \] \<\> 0 は****、MacroError オブジェクトをテスト** します。 If an error has occurred, the error number is non-zero, and the **MessageBox** action runs. The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed. Finally, running the **ClearMacroError** action clears the **MacroError** object.

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
<td><p><strong>[次へ]</strong>に移動 <strong>します。</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow モード</strong>: <strong>Normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: CategoryForm<strong>Record</strong>: Previous</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]。[Number] &lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: = &quot; Error # &quot; &amp; [MacroError].[Number] &amp; &quot; &quot; &amp; on [MacroError].[ActionName] &amp; &quot; アクション。 &quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

