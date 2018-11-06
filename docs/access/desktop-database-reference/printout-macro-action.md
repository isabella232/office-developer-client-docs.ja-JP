---
title: PrintOut マクロ アクション
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c2e5b3e2cdfb743df8a098d3978ccd3d6eb66d90
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999030"
---
# <a name="printout-macro-action"></a>PrintOut マクロ アクション

**適用されます**Access 2013、Office 2013。

**プリント アウト**のアクションを使用するには、開いているデータベースのアクティブ オブジェクトを印刷します。 データシート、レポート、フォーム、データ アクセス ページ、およびモジュールを印刷できます。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="setting"></a>設定値

**印刷**操作では、次の引数があります。

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
<td><p><strong>Print Range/印刷範囲</strong></p></td>
<td><p>印刷する範囲。 <strong>すべて</strong>(ユーザーが印刷のすべてのオブジェクト)、<strong>選択範囲</strong>(ユーザーが選択されているオブジェクトの一部を印刷できます)、または<strong>ページ</strong>(ユーザーはページの範囲を<strong>ページから</strong><strong>ページへ</strong>の引数に指定できます) をクリックして、<strong>で印刷範囲</strong>、[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションのボックスです。 既定値は [ <strong>すべてのレコード</strong>] です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Page From/開始ページ</strong></p></td>
<td><p>印刷する最初のページを指定します。このページの先頭から印刷が開始されます。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Page To/終了ページ</strong></p></td>
<td><p>印刷する最後のページを指定します。このページの最後で印刷が終了します。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Print Quality/印刷品質</strong></p></td>
<td><p>印刷の品質を指定します。[ <strong>高</strong>]、[ <strong>中</strong>]、[ <strong>低</strong>]、[ <strong>簡易</strong>] のいずれかをクリックします。印刷の品質が低いほど、速く印刷されます。既定値は [ <strong>高</strong>] です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Copies/部数</strong></p></td>
<td><p>印刷部数を指定します。既定値は 1 です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Collate Copies/部単位で印刷</strong></p></td>
<td><p>部単位で印刷する場合は [はい]、部単位で印刷しない場合は [いいえ] をクリックします。この引数を [いいえ] に設定すると、[はい] の場合より速く印刷できます。既定値は [はい] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

このアクションの動作は、オブジェクトを選択し、[ **ファイル**] タブをクリックして、[ **印刷**] をクリックした場合と同じです。ただし、このアクションを使用する場合は、[ **印刷**] ダイアログ ボックスは表示されません。

> [!TIP]
> 頻繁に使用する特定の印刷設定をした場合は、引数内のこれらの設定で**プリント アウト**のアクションを含むマクロを作成します。

このアクションの引数は、[**印刷**] ダイアログ ボックスのオプションに対応しています。 ただし、操作を**行って** **[検索し、置換**] ダイアログ ボックスとは異なり引数の設定値とは共用されません、 **[印刷**] ダイアログ ボックスのオプションです。

Visual Basic for Applications (VBA) モジュールの**印刷**操作を実行するには、 **DoCmd**オブジェクトの**PrintOut**メソッドを使用します。

