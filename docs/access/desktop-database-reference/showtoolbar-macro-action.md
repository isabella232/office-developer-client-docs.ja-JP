---
title: "'ShowToolbar/ツール バーの表示' マクロ アクション"
TOCTitle: ShowToolbar Macro Action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 462dbd34f5666643cceff1fc96b9dd77c36d0071
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477663"
---
# <a name="showtoolbar-macro-action"></a>"ShowToolbar/ツール バーの表示" マクロ アクション


**適用されます**Access 2013 |。Office 2013

**[アドイン**] タブのコマンドのグループを表示または非表示に**切り替えます**を使用することができます。


> [!NOTE]
> <P><STRONG>ShowToolbar</STRONG>アクションは、ショートカット メニューには影響しません。</P>




> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

**ShowToolbar**アクションには、次の引数があります。

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
<td><p><strong>Toolbar Name/ツール バー名</strong></p></td>
<td><p><strong>[アドイン</strong>] タブ上のコマンド グループの名前を表示または非表示にします。 マクロ ビルダー] ウィンドウの [<strong>ツールバー名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、この操作によって影響を受けることができますすべての利用可能なグループを示しています。 この引数は省略できません。 ライブラリ データベースで<strong>ShowToolbar</strong>アクションを含むマクロを実行する場合は、まずライブラリ データベースで、[し、[現在のデータベース内にこの名前のグループの検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>表示または非表示] グループにあるかどうか、およびどのビューで表示または非表示にするを指定します。 既定値は<strong>[はい]</strong> (常にグループを表示するです)。 時間、<strong>適切な場所</strong>に適切なフォームまたはレポートがアクティブなときにのみ、グループを表示] または [<strong>いいえ</strong>常にグループを非表示にするすべてのグループを表示するには、 <strong>[はい]</strong>を選択します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

マクロでこのアクションと条件式を組み合わせて使用すると、特定の条件に応じてグループの表示と非表示を切り替えることができます。

1 つのフォームまたはレポート上の特定のグループを表示する場合は、グループを表示する**ShowToolbar**のアクションを含むマクロの名前に、フォームまたはレポートの**OnActivate**プロパティを設定できます。 グループを非表示にする**ShowToolbar**のアクションを含むマクロの名前に、フォームまたはレポートの**OnDeactivate**プロパティを設定します。

組み込みのツールバーでは利用できない**できるようにする組み込みのツールバーを表示**] オプションを設定する場合または**False** (0) で、Visual Basic for Applications (VBA) のモジュールに**できない**プロパティを設定する場合にこのアクションを使用して非表示**False** **SetOption**メソッドを使用して VBA にします。

VBA モジュールで**ShowToolbar**アクションを実行するには、 **DoCmd**オブジェクトの**ShowToolbar**メソッドを使用します。

