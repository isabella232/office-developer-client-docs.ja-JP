---
title: LogEvent マクロ アクション
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edc2fcaa72f6bfb912708948903aa09b25447580
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998175"
---
# <a name="logevent-macro-action"></a>LogEvent マクロ アクション

**適用されます**Access 2013、Office 2013。

**LogEvent**アクションは、 **USysApplicationLog**システム ・ テーブルに情報を書き込みます。

> [!NOTE]
> **LogEvent**アクションは、データ マクロでのみ使用可能。

## <a name="setting"></a>設定

**LogEvent**アクションには、次の引数があります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Description</strong></p></td>
<td><p>いいえ</p></td>
<td><p>記録する条件を説明する文字列式を指定します。説明は 255 文字以内とします。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>備考

**[RaiseError](raiseerror-macro-action.md)** アクションを使用して、エラーをスローする価値がない**USysApplicationLog**システム ・ テーブルに状態情報を書き込むには、 **LogEvent**アクションを使用できます。 たとえば、特定のフィールドに変更をログに記録または**USysApplicationLog**に書き込む項目を使用して、マクロのデバッグを支援するためできます。

**LogEvent**アクションを使用して、 **USysApplicationLog**テーブルへの書き込み、**ユーザー**に **[カテゴリ**] 列が自動的に設定します。

**USysApplicationLog**テーブルを表示するには、次の手順に従います。

1.  [ **ファイル**] メニューの [ **オプション**] をクリックします。

2.  [ **Access のオプション**] ダイアログ ボックスで [ **カレント データベース**] タブをクリックします。

3.  [ **ナビゲーション**] セクションで [ **ナビゲーション オプション**] をクリックします。

4.  [ **ナビゲーション オプション**] ダイアログ ボックスで [ **システム オブジェクトの表示**] をクリックし、[ **OK**] をクリックします。

5.  [ **OK**] をクリックして [ **Access のオプション**] ダイアログ ボックスを終了します。

