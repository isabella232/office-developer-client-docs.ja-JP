---
title: "\"CloseWindow/ウィンドウを閉じる\" マクロ アクション"
TOCTitle: CloseWindow Macro Action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1d80ac5b545f07d3bd39f69f16c4578e49439cdf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476262"
---
# <a name="closewindow-macro-action"></a>"CloseWindow/ウィンドウを閉じる" マクロ アクション


**適用されます**Access 2013 |。Office 2013

" **CloseWindow/ウィンドウを閉じる** " アクションを使用すると、指定した Access ドキュメント タブを閉じることができます。何も指定しない場合は、アクティブなドキュメント タブが閉じます。

## <a name="setting"></a>設定値

**CloseWindow**アクションには、次の引数があります。

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
<td><p>ドキュメント タブを閉じるオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスの一覧で [ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。アクティブなドキュメント タブを選択する場合は、この引数を指定しません。  </p>

> [!NOTE]
> <P>モジュールでは、Visual Basic エディターを終了する場合、<STRONG>オブジェクトの型</STRONG>引数に<STRONG>モジュール</STRONG>を使用する必要があります。</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name/オブジェクト名</strong></p></td>
<td><p>閉じるオブジェクトの名前。 [ <strong>オブジェクト名</strong> ] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。 閉じるオブジェクトをクリックします。 <strong>オブジェクトの型</strong>引数を空白のままにする場合は、この引数を指定しないも。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save/オブジェクトの保存</strong></p></td>
<td><p>オブジェクトを閉じるときに、オブジェクトに加えた変更を保存するかどうかを指定します。保存する場合は [ <strong>する</strong>]、保存せずに閉じる場合は [ <strong>しない</strong>]、保存するかどうかを毎回確認する場合は [ <strong>確認</strong>] をクリックします。既定値は [ <strong>確認</strong>] です。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**CloseWindow**アクションは、すべてのユーザーが明示的に開くことができるデータベース オブジェクトまたは閉じる動作します。 このアクションは、オブジェクトを選択して、オブジェクトのドキュメント タブを右クリックして [ショートカット] メニューの [**閉じる**] をクリックしてしたり、オブジェクトの**閉じる**ボタンをクリックして終了すると同じ効果を持ちます。

**保存**引数は、**プロンプト**に設定されて、 **CloseWindow**アクションを実行する前にオブジェクトが保存されていない場合は、マクロが終了する前にオブジェクトを保存するのにを求めるダイアログ ボックスが表示されます。 **よって**の**警告の**引数を**No**に設定した場合ダイアログ ボックスが表示されないと、オブジェクトが自動的に保存します。

**CloseWindow**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**CloseWindow**メソッドを使用します。

