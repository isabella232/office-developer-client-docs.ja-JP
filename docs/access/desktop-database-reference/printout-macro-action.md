---
title: "\"PrintOut/印刷\" マクロ アクション"
TOCTitle: PrintOut Macro Action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6a0aa0ae6d992410d5bed6126bfe49d7e84e9135
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878732"
---
# <a name="printout-macro-action"></a><span data-ttu-id="bca70-102">"PrintOut/印刷" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="bca70-102">PrintOut Macro Action</span></span>


<span data-ttu-id="bca70-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bca70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bca70-104">**プリント アウト**のアクションを使用するには、開いているデータベースのアクティブ オブジェクトを印刷します。</span><span class="sxs-lookup"><span data-stu-id="bca70-104">You can use the **PrintOut** action to print the active object in the open database.</span></span> <span data-ttu-id="bca70-105">データシート、レポート、フォーム、データ アクセス ページ、およびモジュールを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="bca70-105">You can print datasheets, reports, forms, data access pages, and modules.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bca70-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bca70-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="bca70-108">設定値</span><span class="sxs-lookup"><span data-stu-id="bca70-108">Setting</span></span>

<span data-ttu-id="bca70-109">**印刷**操作では、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="bca70-109">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bca70-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="bca70-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bca70-111">説明</span><span class="sxs-lookup"><span data-stu-id="bca70-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bca70-112"><strong>Print Range/印刷範囲</strong></span><span class="sxs-lookup"><span data-stu-id="bca70-112"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="bca70-113">印刷する範囲。</span><span class="sxs-lookup"><span data-stu-id="bca70-113">The range to print.</span></span> <span data-ttu-id="bca70-114"><strong>すべて</strong>(ユーザーが印刷のすべてのオブジェクト)、<strong>選択範囲</strong>(ユーザーが選択されているオブジェクトの一部を印刷できます)、または<strong>ページ</strong>(ユーザーはページの範囲を<strong>ページから</strong><strong>ページへ</strong>の引数に指定できます) をクリックして、<strong>で印刷範囲</strong>、[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションのボックスです。</span><span class="sxs-lookup"><span data-stu-id="bca70-114">Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="bca70-115">既定値は [ <strong>すべてのレコード</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="bca70-115">The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bca70-116"><strong>Page From/開始ページ</strong></span><span class="sxs-lookup"><span data-stu-id="bca70-116"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="bca70-p104">印刷する最初のページを指定します。このページの先頭から印刷が開始されます。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="bca70-p104">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bca70-120"><strong>Page To/終了ページ</strong></span><span class="sxs-lookup"><span data-stu-id="bca70-120"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="bca70-p105">印刷する最後のページを指定します。このページの最後で印刷が終了します。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="bca70-p105">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bca70-124"><strong>Print Quality/印刷品質</strong></span><span class="sxs-lookup"><span data-stu-id="bca70-124"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="bca70-p106">印刷の品質を指定します。[ <strong>高</strong>]、[ <strong>中</strong>]、[ <strong>低</strong>]、[ <strong>簡易</strong>] のいずれかをクリックします。印刷の品質が低いほど、速く印刷されます。既定値は [ <strong>高</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="bca70-p106">The print quality. Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>. The lower the quality, the faster the object prints. The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bca70-129"><strong>Copies/部数</strong></span><span class="sxs-lookup"><span data-stu-id="bca70-129"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="bca70-p107">印刷部数を指定します。既定値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="bca70-p107">The number of copies to print. The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bca70-132"><strong>Collate Copies/部単位で印刷</strong></span><span class="sxs-lookup"><span data-stu-id="bca70-132"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="bca70-p108">部単位で印刷する場合は [はい]、部単位で印刷しない場合は [いいえ] をクリックします。この引数を [いいえ] に設定すると、[はい] の場合より速く印刷できます。既定値は [はい] です。</span><span class="sxs-lookup"><span data-stu-id="bca70-p108">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bca70-136">解説</span><span class="sxs-lookup"><span data-stu-id="bca70-136">Remarks</span></span>

<span data-ttu-id="bca70-p109">このアクションの動作は、オブジェクトを選択し、[ **ファイル**] タブをクリックして、[ **印刷**] をクリックした場合と同じです。ただし、このアクションを使用する場合は、[ **印刷**] ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="bca70-p109">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>


> [!TIP]
> <P><span data-ttu-id="bca70-139">頻繁に使用する特定の印刷設定をした場合は、引数内のこれらの設定で<STRONG>プリント アウト</STRONG>のアクションを含むマクロを作成します。</span><span class="sxs-lookup"><span data-stu-id="bca70-139">If you have particular print settings you use frequently, create a macro containing a <STRONG>PrintOut</STRONG> action with these settings in its arguments.</span></span></P>



<span data-ttu-id="bca70-140">このアクションの引数は、[**印刷**] ダイアログ ボックスのオプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="bca70-140">The arguments for this action correspond to options in the **Print** dialog box.</span></span> <span data-ttu-id="bca70-141">ただし、操作を**行って** **[検索し、置換**] ダイアログ ボックスとは異なり引数の設定値とは共用されません、 **[印刷**] ダイアログ ボックスのオプションです。</span><span class="sxs-lookup"><span data-stu-id="bca70-141">However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="bca70-142">Visual Basic for Applications (VBA) モジュールの**印刷**操作を実行するには、 **DoCmd**オブジェクトの**PrintOut**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="bca70-142">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

