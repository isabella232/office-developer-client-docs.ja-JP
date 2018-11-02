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
ms.openlocfilehash: 74d3c050b7d3912c6b0b369f99ca163cee87643a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919711"
---
# <a name="findrecord-macro-action"></a><span data-ttu-id="e2e4d-102">FindRecord マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="e2e4d-102">FindRecord macro action</span></span>


<span data-ttu-id="e2e4d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2e4d-p101">**FindRecord** アクションは、 **FindRecord/レコードの検索** 引数で指定した抽出条件を満たす最初のデータのインスタンスを検索するために使用します。カレント レコード、次のレコード、前のレコード、または最初のレコードのデータに対する検索で使用できます。アクティブなテーブル データシート、クエリ データシート、フォーム データシート、またはフォームのレコードを検索できます。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p101">You can use the **FindRecord** action to find the first instance of data that meets the criteria specified by the **FindRecord** arguments. This data can be in the current record, in a succeeding or prior record, or in the first record. You can find records in the active table datasheet, query datasheet, form datasheet, or form.</span></span>

## <a name="setting"></a><span data-ttu-id="e2e4d-107">設定</span><span class="sxs-lookup"><span data-stu-id="e2e4d-107">Setting</span></span>

<span data-ttu-id="e2e4d-108">**FindRecord** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-108">The **FindRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2e4d-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="e2e4d-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e2e4d-110">説明</span><span class="sxs-lookup"><span data-stu-id="e2e4d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2e4d-111"><strong>Find What/検索する文字列</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-111"><strong>Find What</strong></span></span></p></td>
<td><p><span data-ttu-id="e2e4d-112">レコードを検索するデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-112">Specifies the data you want to find in the record.</span></span> <span data-ttu-id="e2e4d-113">テキスト、数値、または、等号 (=) に続く式を入力日付を入力してください (<strong>=</strong>)、[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションで<strong>[検索する文字列</strong>ボックスします。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-113">Enter the text, number, or date you want to find or type an expression, which is preceded by an equal sign (<strong>=</strong>), in the <strong>Find What</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="e2e4d-114">ワイルドカード文字を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-114">You can use wildcard characters.</span></span> <span data-ttu-id="e2e4d-115">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2e4d-116"><strong>Match/検索条件</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-116"><strong>Match</strong></span></span></p></td>
<td><p><span data-ttu-id="e2e4d-p103">フィールドのどの部分を検索するかを指定します。フィールドの一部 ([<strong>フィールドの一部分</strong>])、全体 ([<strong>フィールド全体</strong>])、または先頭 ([<strong>フィールドの先頭</strong>]) を対象にデータを検索するよう指定できます。既定値は [<strong>フィールド全体</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p103">Specifies where the data is located in the field. You can specify a search for data in any part of the field (<strong>Any Part of Field</strong>), for data that fills the entire field (<strong>Whole Field</strong>), or for data located at the beginning of the field (<strong>Start of Field</strong>). The default is <strong>Whole Field</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2e4d-120"><strong>Match Case/大文字/小文字を区別する</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-120"><strong>Match Case</strong></span></span></p></td>
<td><p><span data-ttu-id="e2e4d-p104">大文字と小文字を区別して検索するかどうかを指定します。大文字と小文字を区別する場合は [ <strong>はい</strong>]、区別しない場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>いいえ</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="e2e4d-p104">Specifies whether the search is case-sensitive. Click <strong>Yes</strong> (conduct a case-sensitive search) or <strong>No</strong> (search without matching uppercase and lowercase letters exactly). The default is <strong>No</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2e4d-124"><strong>Search/検索</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-124"><strong>Search</strong></span></span></p></td>
<td><p><span data-ttu-id="e2e4d-p105">カレント レコードから先頭のレコードに向かって検索するか ([<strong>上へ</strong>])、末尾のレコードに向かって検索するか ([<strong>下へ</strong>])、レコードの末尾に向かって検索した後にレコードの先頭からカレント レコードに向かって検索して、すべてのレコードを検索するか ([<strong>すべてのレコード</strong>]) を指定します。既定値は [<strong>すべてのレコード</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p105">Specifies whether the search proceeds from the current record up to the beginning of the records (<strong>Up</strong>); down to the end of the records (<strong>Down</strong>); or down to the end of the records and then from the beginning of the records to the current record, so all records are searched (<strong>All</strong>). The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2e4d-127"><strong>Search As Formatted/表示書式で検索</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-127"><strong>Search As Formatted</strong></span></span></p></td>
<td><p><span data-ttu-id="e2e4d-p106">表示書式でデータを検索するかどうかを指定します。Microsoft Office Access 2007 で、フィールドに表示されている書式でデータを検索する場合は [ <strong>はい</strong>] を、データベースに格納されている形式 (表示されている形式とは異なる場合があります) で検索する場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>いいえ</strong>] です。この機能を使用すると、特定の書式のデータだけを検索することができます。たとえば、コンマが含まれる書式が設定されたフィールドで "1,234" の値を検索する場合は、[ <strong>はい</strong>] をクリックし、" <strong>Find What/検索データ</strong> " 引数に「 <strong>1,234</strong> 」と入力します。「 <strong>1234</strong>」と入力してこのフィールドでデータを検索する場合は、[ <strong>いいえ</strong>] をクリックします。日付の検索では、2003-07-08 のような書式が設定された日付を検索する場合は [ <strong>はい</strong>] をクリックします。[ <strong>いいえ</strong>] をクリックした場合は、Windows コントロール パネルの地域の設定で設定されている書式を使って " <strong>Find What/検索データ</strong> " 引数を入力します。この書式は、地域の設定の [ <strong>日付</strong>] タブにある [ <strong>短い形式</strong>] ボックスに表示されています。たとえば、[ <strong>短い形式</strong>] ボックスに [ <strong>yy/M/d</strong>] が設定されている場合は、「03/7/8」と入力すると、このフィールドの書式にかかわらず、2003 年 7 月 8 日に対応する [日付] フィールドのすべてのエントリが検索されます。  </span><span class="sxs-lookup"><span data-stu-id="e2e4d-p106">Specifies whether the search includes formatted data. Click <strong>Yes</strong> (Microsoft Office Access 2007 searches for the data as it is formatted and displayed in the field) or <strong>No</strong> (Access searches for the data as it is stored in the database, which isn't always the same as it's displayed). The default is <strong>No</strong>. You can use this feature to restrict the search to data in a particular format. For example, click <strong>Yes</strong> and type <strong>1,234</strong> in the <strong>Find What</strong> argument to find a value of 1,234 in a field formatted to include commas. Click <strong>No</strong> if you want to type <strong>1234</strong> to search for the data in this field. To search for dates, click <strong>Yes</strong> to find a date exactly as it is formatted, such as 08-July-2003. If you click <strong>No</strong>, enter the date for the <strong>Find What</strong> argument in the format that is set in the regional settings in Windows Control Panel. This format is shown in the <strong>Short date format</strong> box found on the <strong>Date</strong> tab in the regional settings. For example, if the <strong>Short date format</strong> box is set to <strong>M/d/yy</strong>, you can enter 7/8/03, and Access will find all entries in a Date field that correspond to July 8, 2003, regardless of how this field is formatted.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="e2e4d-138"><STRONG>Search As Formatted/表示書式で検索</STRONG>引数が有効になるのは、カレント フィールドが連結コントロールであること、<STRONG>Match/検索条件</STRONG>引数に [<STRONG>フィールド全体</STRONG>] が設定されていること、<STRONG>Only Current Field/カレント フィールドのみ検索</STRONG>引数に [<STRONG>はい</STRONG>] が設定されていること、および <STRONG>Match Case/大小文字区別</STRONG>引数に [<STRONG>いいえ</STRONG>] が設定されている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-138">The <STRONG>Search As Formatted</STRONG> argument takes effect only if the current field is a bound control, the <STRONG>Match</STRONG> argument is set to <STRONG>Whole Field</STRONG>, the <STRONG>Only Current Field</STRONG> argument is set to <STRONG>Yes</STRONG>, and the <STRONG>Match Case</STRONG> argument is set to <STRONG>No</STRONG>.</span></span></P>


<p><span data-ttu-id="e2e4d-139"><strong>Match Case/大小文字区別</strong>引数を [<strong>はい</strong>] に設定した場合、または <strong>Only Current Field/カレント フィールドのみ検索</strong>引数を [<strong>いいえ</strong>] に設定した場合は、<strong>Search As Formatted/表示書式で検索</strong>引数を [<strong>はい</strong>] に設定する必要があります。

</span><span class="sxs-lookup"><span data-stu-id="e2e4d-139">If you set <strong>Match Case</strong> to <strong>Yes</strong> or <strong>Only Current Field</strong> to <strong>No</strong>, you must also set <strong>Search As Formatted</strong> to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2e4d-140"><strong>Only Current Field/カレント フィールドのみ</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-140"><strong>Only Current Field</strong></span></span></p></td>
<td><p><span data-ttu-id="e2e4d-p107">各レコードのカレント フィールドだけで検索するか、または各レコードのすべてのフィールドで検索するかを指定します。カレント フィールドを検索する方が速くなります。カレント フィールドだけで検索する場合は [ <strong>はい</strong>] をクリックし、各レコードのすべてのフィールドで検索する場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>はい</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="e2e4d-p107">Specifies whether the search is confined to the current field in each record or includes all fields in each record. Searching in the current field is faster. Click <strong>Yes</strong> (confine the search to the current field) or <strong>No</strong> (search in all fields in each record). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2e4d-145"><strong>Find First/先頭から検索</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-145"><strong>Find First</strong></span></span></p></td>
<td><p><span data-ttu-id="e2e4d-p108">先頭のレコードから検索を開始するか、カレント レコードから検索を開始するかを指定します。先頭のレコードから開始する場合は [ <strong>はい</strong>] をクリックし、カレント レコードから開始する場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>はい</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="e2e4d-p108">Specifies whether the search starts at the first record or at the current record. Click <strong>Yes</strong> (start at the first record) or <strong>No</strong> (start at the current record). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e2e4d-149">解説</span><span class="sxs-lookup"><span data-stu-id="e2e4d-149">Remarks</span></span>

<span data-ttu-id="e2e4d-p109">マクロの **FindRecord** アクションが実行されると、各レコードで指定データが検索されます (検索順序は **Search/検索** 引数の設定値によって決まります)。指定データが見つかると、そのレコードの該当データが選択されます。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p109">When a macro runs the **FindRecord** action, Access searches for the specified data in the records (the order of the search is determined by the setting of the **Search** argument). When Access finds the specified data, the data is selected in the record.</span></span>

<span data-ttu-id="e2e4d-p110">**FindRecord** アクションの動作は、[ **ホーム**] タブの [ **検索**] をクリックした場合と同じで、その引数は [ **検索と置換**] ダイアログ ボックスのオプションと同じです。[マクロ ビルダー] ウィンドウで **FindRecord/レコードの検索** 引数を設定してからマクロを実行した場合、[ **検索**] をクリックしたときに [ **検索と置換**] ダイアログ ボックスで、対応する各オプションが選択されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p110">The **FindRecord** action is equivalent to clicking **Find** on the **Home** tab, and its arguments are the same as the options in the **Find and Replace** dialog box. If you set the **FindRecord** arguments in the Macro Builder pane and then run the macro, you will see the corresponding options selected in the **Find and Replace** dialog box when you click **Find**.</span></span>

<span data-ttu-id="e2e4d-p111">データベースの操作中は、直近の **FindRecord/レコードの検索** 引数が保持されるので、次に **FindRecord** アクションを使用するときに、同じ検索条件を繰り返し入力する必要はありません。引数を指定しない場合、前回実行した **FindRecord** アクションまたは [ **検索と置換**] ダイアログ ボックスで最後に設定した引数の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p111">Access retains the most recent **FindRecord** arguments during a database session so that you don't need to enter the same criteria repeatedly as you perform subsequent operations with the **FindRecord** action. If you leave an argument blank, Access uses the most recent setting for the argument, as set either by a previous **FindRecord** action or in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="e2e4d-156">マクロを使ってレコードを検索する場合は、 **RunMenuCommand** アクションの引数の設定によって [ **検索**] コマンドを実行するのではなく、 **FindRecord** アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-156">When you want to find a record by using a macro, use the **FindRecord** action, not the **RunMenuCommand** action with its argument set to run the **Find** command.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e2e4d-p112">[!メモ] <STRONG>FindRecord</STRONG> アクションは、テーブル、クエリ、およびフォームでは [ <STRONG>ホーム</STRONG>] タブの [ <STRONG>検索</STRONG>] コマンドに対応していますが、コード ウィンドウでは [ <STRONG>編集</STRONG>] メニューの [ <STRONG>検索</STRONG>] コマンドに対応していません。 <STRONG>FindRecord</STRONG> アクションで、モジュール内のテキストを検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p112">While the <STRONG>FindRecord</STRONG> action corresponds to the <STRONG>Find</STRONG> command on the <STRONG>Home</STRONG> tab for tables, queries, and forms, it doesn't correspond to the <STRONG>Find</STRONG> command on the <STRONG>Edit</STRONG> menu in the Code window. You can't use the <STRONG>FindRecord</STRONG> action to search for text in modules.</span></span></P>



<span data-ttu-id="e2e4d-p113">現在選択されているテキストが、 **FindRecord** アクション実行時の検索テキストと同じである場合は、同じレコードの同じフィールドの、選択されているテキストの直後から検索が開始されます。選択されているテキストと検索テキストが異なる場合は、カレント レコードの先頭から検索が開始されます。このため、1 つのレコードに同じ検索条件を満たすテキストが複数存在する場合の検索が可能です。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p113">If the currently selected text is the same as the search text at the time the **FindRecord** action is carried out, the search begins immediately following the selection in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="e2e4d-p114">ただし、コマンド ボタンを使って、 **FindRecord** アクションが含まれているマクロを実行する場合は、検索条件を満たす最初のテキストが繰り返し検索されます。これは、コマンド ボタンをクリックしたときに、検索条件を満たす値が含まれるフィールドからフォーカスが変更されるためです。その結果、 **FindRecord** アクションによる検索はレコードの先頭から再開されます。この問題を回避するには、フォーカスを変更しない方法を使ってマクロを実行します。たとえば、カスタム ツール バー ボタン、AutoKeys マクロで定義されたキーの組み合わせなどを使用します。または **FindRecord** アクションを実行する前に、検索条件が含まれるフィールドにフォーカスを設定するようにマクロを変更します。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p114">However, note that if you use a command button to run a macro containing the **FindRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro, or set the focus in the macro to the field containing the search criteria before you carry out the **FindRecord** action.</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティに関する注意" alt="Security note" /><span data-ttu-id="e2e4d-167"><strong>セキュリティ メモ</strong></span><span class="sxs-lookup"><span data-stu-id="e2e4d-167"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2e4d-p115">
      重要な情報または機密情報には <strong>SendKeys</strong> ステートメントまたは AutoKeys マクロを使用しないでください。悪意のあるユーザーがキー入力を途中で遮り、コンピューターおよびデータのセキュリティを侵害するおそれがあります。
</span><span class="sxs-lookup"><span data-stu-id="e2e4d-p115">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2e4d-170">コマンド ボタンを使って、 **FindNext** アクションが含まれているマクロを実行する場合も、同様の問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-170">The same behavior also occurs if you use a command button to run a macro containing the **FindNext** action.</span></span>

<span data-ttu-id="e2e4d-171">Visual Basic for Applications (VBA) モジュールで **FindRecord** アクションを実行するには、 **DoCmd** オブジェクトの **FindRecord** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-171">To run the **FindRecord** action in a Visual Basic for Applications (VBA) module, use the **FindRecord** method of the **DoCmd** object.</span></span>

<span data-ttu-id="e2e4d-172">複雑な検索の場合は、 **SearchForRecord** マクロ アクションを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="e2e4d-172">For more complex searches, you may want to use the **SearchForRecord** macro action.</span></span>

