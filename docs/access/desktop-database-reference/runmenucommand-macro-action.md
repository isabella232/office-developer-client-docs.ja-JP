---
title: RunMenuCommand マクロ アクション
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 405d2d69666f6ebe9065ea6656e3fe1b4192153b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562245"
---
# <a name="runmenucommand-macro-action"></a>RunMenuCommand マクロ アクション

**適用先:** Access 2013、Office 2013

"RunMenuCommand/メニューコマンドの実行" アクションを使用すると、組み込みの Microsoft Access コマンドを実行できます。

## <a name="setting"></a>設定

"RunMenuCommand/メニューコマンドの実行" アクションの引数は次のとおりです。

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
<td><p><strong>Command</strong></p></td>
<td><p>実行するコマンドの名前を指定します。[<strong>コマンド</strong>] ボックスには、Access の使用可能な組み込みのコマンドが五十音順で表示されます。この引数は省略できません。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

"RunMenuCommand/メニューコマンドの実行" アクションを使用すると、Access コマンドをカスタム メニュー バー、グローバル メニュー バー、カスタム ショートカット メニュー、またはグローバル ショートカット メニューから実行できます。

You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.

> [!NOTE]
> Clicking the **File** tab and then clicking **Recent** shows the most recently used databases. You can click one of these databases instead of clicking **Open**. These database items don't appear in the drop-down list box for the **Command** argument, and aren't available by using the **RunMenuCommand** action in a macro.

When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.

To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)

