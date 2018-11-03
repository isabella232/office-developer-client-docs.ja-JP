---
title: FindRecord マクロ アクション
TOCTitle: FindRecord macro action
ms:assetid: 379e3dda-cb7d-a294-29b1-c6ce9a62ba8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192494(v=office.15)
ms:contentKeyID: 48544199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm7496
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 19b6c80af2bcee9ca3dbe51bbbcf56343f33d550
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937611"
---
# <a name="findrecord-macro-action"></a>FindRecord マクロ アクション

**適用されます**Access 2013、Office 2013。

**FindRecord** アクションは、 **FindRecord/レコードの検索** 引数で指定した抽出条件を満たす最初のデータのインスタンスを検索するために使用します。カレント レコード、次のレコード、前のレコード、または最初のレコードのデータに対する検索で使用できます。アクティブなテーブル データシート、クエリ データシート、フォーム データシート、またはフォームのレコードを検索できます。

## <a name="setting"></a>設定

**FindRecord** アクションの引数は次のとおりです。

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
<td><p><strong>Find What/検索する文字列</strong></p></td>
<td><p>レコードを検索するデータを指定します。 テキスト、数値、または、等号 (=) に続く式を入力日付を入力してください (<strong>=</strong>)、[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションで<strong>[検索する文字列</strong>ボックスします。 ワイルドカード文字を使用することができます。 この引数は省略できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Match/検索条件</strong></p></td>
<td><p>フィールドのどの部分を検索するかを指定します。フィールドの一部 ([<strong>フィールドの一部分</strong>])、全体 ([<strong>フィールド全体</strong>])、または先頭 ([<strong>フィールドの先頭</strong>]) を対象にデータを検索するよう指定できます。既定値は [<strong>フィールド全体</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Match Case/大文字/小文字を区別する</strong></p></td>
<td><p>大文字と小文字を区別して検索するかどうかを指定します。大文字と小文字を区別する場合は [ <strong>はい</strong>]、区別しない場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>いいえ</strong>] です。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Search/検索</strong></p></td>
<td><p>カレント レコードから先頭のレコードに向かって検索するか ([<strong>上へ</strong>])、末尾のレコードに向かって検索するか ([<strong>下へ</strong>])、レコードの末尾に向かって検索した後にレコードの先頭からカレント レコードに向かって検索して、すべてのレコードを検索するか ([<strong>すべてのレコード</strong>]) を指定します。既定値は [<strong>すべてのレコード</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Search As Formatted/表示書式で検索</strong></p></td>
<td><p>表示書式でデータを検索するかどうかを指定します。Microsoft Office Access 2007 で、フィールドに表示されている書式でデータを検索する場合は [ <strong>はい</strong>] を、データベースに格納されている形式 (表示されている形式とは異なる場合があります) で検索する場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>いいえ</strong>] です。この機能を使用すると、特定の書式のデータだけを検索することができます。たとえば、コンマが含まれる書式が設定されたフィールドで "1,234" の値を検索する場合は、[ <strong>はい</strong>] をクリックし、" <strong>Find What/検索データ</strong> " 引数に「 <strong>1,234</strong> 」と入力します。「 <strong>1234</strong>」と入力してこのフィールドでデータを検索する場合は、[ <strong>いいえ</strong>] をクリックします。日付の検索では、2003-07-08 のような書式が設定された日付を検索する場合は [ <strong>はい</strong>] をクリックします。[ <strong>いいえ</strong>] をクリックした場合は、Windows コントロール パネルの地域の設定で設定されている書式を使って " <strong>Find What/検索データ</strong> " 引数を入力します。この書式は、地域の設定の [ <strong>日付</strong>] タブにある [ <strong>短い形式</strong>] ボックスに表示されています。たとえば、[ <strong>短い形式</strong>] ボックスに [ <strong>yy/M/d</strong>] が設定されている場合は、「03/7/8」と入力すると、このフィールドの書式にかかわらず、2003 年 7 月 8 日に対応する [日付] フィールドのすべてのエントリが検索されます。  </p>

> [!NOTE]
> **Search As Formatted/表示書式で検索**引数が有効になるのは、カレント フィールドが連結コントロールであること、**Match/検索条件**引数に [**フィールド全体**] が設定されていること、**Only Current Field/カレント フィールドのみ検索**引数に [**はい**] が設定されていること、および **Match Case/大小文字区別**引数に [**いいえ**] が設定されている場合のみです。


<p><strong>Match Case/大小文字区別</strong>引数を [<strong>はい</strong>] に設定した場合、または <strong>Only Current Field/カレント フィールドのみ検索</strong>引数を [<strong>いいえ</strong>] に設定した場合は、<strong>Search As Formatted/表示書式で検索</strong>引数を [<strong>はい</strong>] に設定する必要があります。

</p></td>
</tr>
<tr class="even">
<td><p><strong>Only Current Field/カレント フィールドのみ</strong></p></td>
<td><p>各レコードのカレント フィールドだけで検索するか、または各レコードのすべてのフィールドで検索するかを指定します。カレント フィールドを検索する方が速くなります。カレント フィールドだけで検索する場合は [ <strong>はい</strong>] をクリックし、各レコードのすべてのフィールドで検索する場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>はい</strong>] です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Find First/先頭から検索</strong></p></td>
<td><p>先頭のレコードから検索を開始するか、カレント レコードから検索を開始するかを指定します。先頭のレコードから開始する場合は [ <strong>はい</strong>] をクリックし、カレント レコードから開始する場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>はい</strong>] です。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

マクロの **FindRecord** アクションが実行されると、各レコードで指定データが検索されます (検索順序は **Search/検索** 引数の設定値によって決まります)。指定データが見つかると、そのレコードの該当データが選択されます。

**FindRecord** アクションの動作は、[ **ホーム**] タブの [ **検索**] をクリックした場合と同じで、その引数は [ **検索と置換**] ダイアログ ボックスのオプションと同じです。[マクロ ビルダー] ウィンドウで **FindRecord/レコードの検索** 引数を設定してからマクロを実行した場合、[ **検索**] をクリックしたときに [ **検索と置換**] ダイアログ ボックスで、対応する各オプションが選択されていることがわかります。

データベースの操作中は、直近の **FindRecord/レコードの検索** 引数が保持されるので、次に **FindRecord** アクションを使用するときに、同じ検索条件を繰り返し入力する必要はありません。引数を指定しない場合、前回実行した **FindRecord** アクションまたは [ **検索と置換**] ダイアログ ボックスで最後に設定した引数の値が使用されます。

マクロを使ってレコードを検索する場合は、 **RunMenuCommand** アクションの引数の設定によって [ **検索**] コマンドを実行するのではなく、 **FindRecord** アクションを使用します。

> [!NOTE]
> [!メモ] **FindRecord** アクションは、テーブル、クエリ、およびフォームでは [ **ホーム**] タブの [ **検索**] コマンドに対応していますが、コード ウィンドウでは [ **編集**] メニューの [ **検索**] コマンドに対応していません。 **FindRecord** アクションで、モジュール内のテキストを検索することはできません。

現在選択されているテキストが、 **FindRecord** アクション実行時の検索テキストと同じである場合は、同じレコードの同じフィールドの、選択されているテキストの直後から検索が開始されます。選択されているテキストと検索テキストが異なる場合は、カレント レコードの先頭から検索が開始されます。このため、1 つのレコードに同じ検索条件を満たすテキストが複数存在する場合の検索が可能です。

ただし、コマンド ボタンを使って、 **FindRecord** アクションが含まれているマクロを実行する場合は、検索条件を満たす最初のテキストが繰り返し検索されます。これは、コマンド ボタンをクリックしたときに、検索条件を満たす値が含まれるフィールドからフォーカスが変更されるためです。その結果、 **FindRecord** アクションによる検索はレコードの先頭から再開されます。この問題を回避するには、フォーカスを変更しない方法を使ってマクロを実行します。たとえば、カスタム ツール バー ボタン、AutoKeys マクロで定義されたキーの組み合わせなどを使用します。または **FindRecord** アクションを実行する前に、検索条件が含まれるフィールドにフォーカスを設定するようにマクロを変更します。

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティに関する注意" alt="Security note" /><strong>セキュリティ メモ</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      重要な情報または機密情報には <strong>SendKeys</strong> ステートメントまたは AutoKeys マクロを使用しないでください。悪意のあるユーザーがキー入力を途中で遮り、コンピューターおよびデータのセキュリティを侵害するおそれがあります。
</td>
</tr>
</tbody>
</table>

コマンド ボタンを使って、 **FindNext** アクションが含まれているマクロを実行する場合も、同様の問題が発生します。

Visual Basic for Applications (VBA) モジュールで **FindRecord** アクションを実行するには、 **DoCmd** オブジェクトの **FindRecord** メソッドを使用します。

複雑な検索の場合は、 **SearchForRecord** マクロ アクションを使用することもできます。

