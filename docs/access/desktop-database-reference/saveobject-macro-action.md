---
title: SaveObject マクロ アクション
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 253067d61a496073692ea4e462b9b0a67f0e26cd
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026296"
---
# <a name="saveobject-macro-action"></a>SaveObject マクロ アクション

**適用されます**Access 2013、Office 2013。

**SaveObject**アクションを使用するには指定されていない場合、指定された Access オブジェクトまたはアクティブなオブジェクトのいずれかを保存します。 場合によっては (**クイック アクセス ツールバー**の [名前を**付けて**保存] と同じ機能です) に新しい名前を持つアクティブなオブジェクトを保存することもできます。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="setting"></a>設定値

**SaveObject**アクションには、次の引数があります。

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
<td><p><strong>Object Type/オブジェクトの種類</strong></p></td>
<td><p>保存するオブジェクトの型。 [マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスの一覧で [ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。 アクティブなオブジェクトを選択するには、場合は、この引数を空白のままにします。 この引数でオブジェクト タイプを選択する場合、<strong>オブジェクト名</strong>の引数で既存のオブジェクトの名前を選択します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name/オブジェクト名</strong></p></td>
<td><p>保存するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数を指定せず、この引数も指定しないと、アクティブ オブジェクトが保存されます。この引数に新しい名前を入力すると、アクティブ オブジェクトが入力した名前で保存されます。 新しい名前を入力する場合は、Microsoft Access オブジェクトの名前付け規則に従う必要があります。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**SaveObject**アクションは、保存したりするユーザーが明示的に開くことができるすべてのデータベース オブジェクトに対して動作します。 指定されたオブジェクトは、オブジェクトには影響を**SaveObject**アクションを開く必要があります。 このアクションは、オブジェクトを選択して、**クイック アクセス ツールバー**の**保存**をクリックして保存すると同じ効果を持ちます。 

**オブジェクトの型**引数を指定しないと、[**オブジェクト名**] 引数に新しい名前を入力、**名前を付けて**[**クイック アクセス ツールバー**] をクリックし、アクティブなオブジェクトの新しい名前を入力すると同じ効果を持ちます。 **SaveObject**アクションを使用して保存し、マクロの**名前を付けて保存**コマンドを実行するオブジェクトを指定できます。

> [!NOTE]
> **SaveObject**アクションを使用して、次のいずれかを新しい名前で保存できません。
> - フォーム ビューまたはデータシート ビューのフォーム
> - 印刷プレビューでレポート
> - モジュール
> - データシート ビューまたは印刷プレビューで、[サーバー] ビュー
> - ページ ビューで、データ アクセス ページ
> - データシート ビューまたは印刷プレビューでテーブル
> - クエリ データシート ビューまたは印刷プレビューで
> - データシート ビューまたは印刷プレビューでストアド プロシージャ

**SaveObject**アクション、またはライブラリ データベースでは、現在のデータベースで実行するマクロで行われたものであるかどうか常に指定したオブジェクトまたはアクティブ オブジェクト データベースに保存される、オブジェクトが作成されました。

新しい名前を持つアクティブなオブジェクトを保存する名前は、この種類の既存のオブジェクトの名前と同じ場合は、ダイアログ ボックスは、既存のオブジェクトを上書きするかどうかを確認します。 **よって**の**警告の**引数を**No**に設定すると、ダイアログ ボックスが表示されていないし、古いオブジェクトが自動的に上書きされます。

Visual Basic for Applications (VBA) モジュールに**SaveObject**アクションを実行するには、 **DoCmd**オブジェクトの**Save**メソッドを使用します。

