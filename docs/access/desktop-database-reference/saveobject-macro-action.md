---
title: "\"SaveObject/オブジェクトの保存\" マクロ アクション"
TOCTitle: SaveObject Macro Action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f5cbb47c8c4b1ecc4990ca53835f8ae9f7ed4d1b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886572"
---
# <a name="saveobject-macro-action"></a>"SaveObject/オブジェクトの保存" マクロ アクション


**適用されます**Access 2013、Office 2013。

**SaveObject**アクションを使用するには指定されていない場合、指定された Access オブジェクトまたはアクティブなオブジェクトのいずれかを保存します。 場合によっては (**クイック アクセス ツールバー**の [名前を**付けて**保存] と同じ機能です) に新しい名前を持つアクティブなオブジェクトを保存することもできます。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



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

**SaveObject**アクションは、保存したりするユーザーが明示的に開くことができるすべてのデータベース オブジェクトに対して動作します。 指定されたオブジェクトは、オブジェクトには影響を**SaveObject**アクションを開く必要があります。 このアクションは、オブジェクトを選択して、**クイック アクセス ツールバー**の**保存**をクリックして保存すると同じ効果を持ちます。 **オブジェクトの型**引数を指定しないと、[**オブジェクト名**] 引数に新しい名前を入力、**名前を付けて**[**クイック アクセス ツールバー**] をクリックし、アクティブなオブジェクトの新しい名前を入力すると同じ効果を持ちます。 **SaveObject**アクションを使用して保存し、マクロの**名前を付けて保存**コマンドを実行するオブジェクトを指定できます。


> [!NOTE]
> <P><STRONG>SaveObject</STRONG>アクションを使用して、次のいずれかを新しい名前で保存できません。</P>



  - フォーム ビューまたはデータシート ビューで開いたフォーム

  - 印刷プレビューで開いたレポート

  - モジュール

  - データシート ビューまたは印刷プレビューで開いたサーバー ビュー

  - ページ ビューで開いたデータ アクセス ページ

  - データシート ビューまたは印刷プレビューで開いたテーブル

  - データシート ビューまたは印刷プレビューで開いたクエリ

  - データシート ビューまたは印刷プレビューで開いたストアド プロシージャ

**SaveObject**アクション、またはライブラリ データベースでは、現在のデータベースで実行するマクロで行われたものであるかどうか常に指定したオブジェクトまたはアクティブ オブジェクト データベースに保存される、オブジェクトが作成されました。

新しい名前を持つアクティブなオブジェクトを保存する名前は、この種類の既存のオブジェクトの名前と同じ場合は、ダイアログ ボックスは、既存のオブジェクトを上書きするかどうかを確認します。 **よって**の**警告の**引数を**No**に設定すると、ダイアログ ボックスが表示されていないし、古いオブジェクトが自動的に上書きされます。

Visual Basic for Applications (VBA) モジュールに**SaveObject**アクションを実行するには、 **DoCmd**オブジェクトの**Save**メソッドを使用します。

