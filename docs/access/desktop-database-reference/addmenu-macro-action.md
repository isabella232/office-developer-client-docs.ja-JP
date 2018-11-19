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
ms.openlocfilehash: d04c98da0ecef1c2323930c74588b7a6a07c2e29
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026268"
---
# <a name="addmenu-macro-action"></a>AddMenu マクロ アクション


**適用されます**Access 2013、Office 2013。

**Addmenu マクロ**の基本的な操作をについて説明します。

作成するのには、**メニューの追加**アクションを使用できます。

- 特定のフォームやレポートに対する、[ **アドイン**] タブのカスタム メニュー。

- フォーム、レポート、またはコントロールのカスタム ショートカット メニュー。フォーム、レポート、またはコントロールで、組み込みショートカット メニューの代わりに表示されます。

- グローバル ショートカット メニュー。グローバル ショートカット メニューは、フォーム、 レポート、またはコントロールのカスタム ショートカット メニューを追加した場合を除き、テーブルやクエリ データシート内のフィールド、フォーム、およびレポートで、組み込みショートカット メニューの代わりに表示されます。

## <a name="setting"></a>設定値

**メニューの追加**アクションでは、次の引数があります。

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
<td><p>たとえば、メニューの名前&quot;レポート コマンド&quot;または&quot;ツール&quot;。 メニューを選択するキーボードを使用できるようにアクセス キーを作成するのには、アンパサンドを入力します (<strong>&amp;</strong>)、アクセス キーに文字の前にします。 <strong>[アドイン</strong>] タブのメニュー名で、この文字が下線付きで表示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Menu Macro Name/メニュー マクロ名</strong></p></td>
<td><p>メニュー コマンドのマクロを含むマクロ グループの名前を指定します。この引数は省略できません。 

</p>
<p><strong>注</strong>: ライブラリ データベースでは、<strong>メニューの追加</strong>アクションを含むマクロを実行すると、Microsoft Office Access 2007 が現在のデータベースだけでは、この名前のマクロ ・ グループの検索します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Status Bar Text/ステータス バー テキスト</strong></p></td>
<td><p>メニュー選択時にステータス バーに表示されるテキストを指定します。ショートカット メニューの場合、この引数は無視されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

Visual Basic for Applications (VBA) モジュールの**メニューの追加**アクションを実行するには、 **DoCmd**オブジェクトの**AddMenu**メソッドを使用します。 **[アドイン**] タブにカスタム メニューを作成するか、カスタム ショートカット メニューをフォーム、レポート、またはコントロールにアタッチするのには、VBA では、 **MenuBar**プロパティまたは**ShortcutMenuBar**プロパティを設定することもできます。 グローバル ショートカット メニューを作成する**アプリケーション**オブジェクトの**ShortcutMenuBar**プロパティを設定することができます。

