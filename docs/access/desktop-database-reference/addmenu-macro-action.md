---
title: AddMenu マクロ アクション
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280274"
---
# <a name="addmenu-macro-action"></a>AddMenu マクロ アクション


**適用先:** Access 2013、Office 2013

This article describes the basic operation of the **AddMenu** macro action.

You can use the **AddMenu** action to create:

- 特定のフォームやレポートに対する、[ **アドイン**] タブのカスタム メニュー。

- フォーム、レポート、またはコントロールのカスタム ショートカット メニュー。フォーム、レポート、またはコントロールで、組み込みショートカット メニューの代わりに表示されます。

- グローバル ショートカット メニュー。グローバル ショートカット メニューは、フォーム、 レポート、またはコントロールのカスタム ショートカット メニューを追加した場合を除き、テーブルやクエリ データシート内のフィールド、フォーム、およびレポートで、組み込みショートカット メニューの代わりに表示されます。

## <a name="setting"></a>Setting

"AddMenu/メニューの追加" アクションの引数は次のとおりです。

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
<td><p><strong>Menu Name/メニュー名</strong></p></td>
<td><p>メニューの名前&quot;(レポートコマンド&quot;や&quot;ツール&quot;など)。 キーボードを使用してメニューを選択できるようにアクセスキーを作成するには、アクセスキー<strong>&amp;</strong>として使用する文字の前にアンパサンド () を入力します。 [<strong>アドイン</strong>] タブのメニュー名で、この文字に下線が付きます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Menu Macro Name/メニュー マクロ名</strong></p></td>
<td><p>メニュー コマンドのマクロを含むマクロ グループの名前を指定します。 この引数は省略できません。</p>
<p><strong>注</strong>: ライブラリデータベースで " <strong>AddMenu/メニュー</strong>の作成" アクションが記述されたマクロを実行すると、Microsoft Office Access 2007 は、この名前のマクログループをカレントデータベースでのみ検索します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Status Bar Text/ステータス バー テキスト</strong></p></td>
<td><p>メニュー選択時にステータス バーに表示されるテキストを指定します。 ショートカット メニューの場合、この引数は無視されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.

