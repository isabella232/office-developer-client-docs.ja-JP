---
title: "'RunMenuCommand/メニューコマンドの実行' マクロ アクション"
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 372803779767ea6fdc12b4e10b5dde231ce101fc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875514"
---
# <a name="runmenucommand-macro-action"></a>"RunMenuCommand/メニューコマンドの実行" マクロ アクション


**適用されます**Access 2013、Office 2013。

**RunMenuCommand**アクションを使用すると、組み込みの Access コマンドを実行します。

## <a name="setting"></a>設定値

**RunMenuCommand**アクションには、次のアクションの引数があります。

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


## <a name="remarks"></a>解説

**RunMenuCommand**アクションを使用すると、カスタム メニュー バー、グローバル メニュー バー、カスタム ショートカット メニューまたはグローバル ショートカット メニューから、Access コマンドを実行します。

マクロ内で条件付き書式**RunMenuCommand**アクションを使用するには一定の条件に従ってコマンドを実行します。


> [!NOTE]
> <P>[<STRONG>ファイル</STRONG>] タブをクリックし、[<STRONG>最近使用した</STRONG>最近使用したデータベースを示しています。 <STRONG>開く</STRONG>をクリックする代わりにこれらのデータベースのいずれかをクリックすることができます。 データベースのこれらの項目は、<STRONG>コマンド</STRONG>の引数のドロップダウン リスト ボックスに表示されないし、 <STRONG>RunMenuCommand</STRONG>アクションを使用してマクロ内で使用できません。</P>



以前のバージョンの Access から Access データベースを変換するときにいくつかのコマンドが利用できなくです。 コマンドでは、可能性がありますが名前が変更されて、別のメニューに移動または、Access で使用可能な不要になった場合があります。 **RunMenuCommand**アクションには、このようなコマンドの動作を**DoMenuItem**を変換できません。 マクロを開くと、このようなコマンドの**コマンド**の引数が空で、 **RunMenuCommand**アクションが表示されます。 マクロを編集、有効なコマンド引数を入力し、または**RunMenuCommand**アクションを削除する必要があります。

**RunMenuCommand**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **Application**オブジェクトの**RunCommand**メソッドを使用します。 (これは、 **DoCmd**オブジェクトの**RunCommand**メソッドと同等) です。

