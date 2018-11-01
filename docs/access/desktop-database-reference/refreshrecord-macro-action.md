---
title: "'RefreshRecord/レコードの更新' マクロ アクション"
TOCTitle: RefreshRecord Macro Action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 65f972f2ec50212685897d496fd072c7d3f57968
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876023"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="e5365-102">"RefreshRecord/レコードの更新" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="e5365-102">RefreshRecord Macro Action</span></span>


<span data-ttu-id="e5365-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e5365-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5365-104">**RefreshRecord**アクションを使用すると、アクティブ フォームまたはアクティブ データシートの現在のセット内のレコードに加えられた変更を反映するために基になるレコード ソースを更新します。</span><span class="sxs-lookup"><span data-stu-id="e5365-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5365-105">備考</span><span class="sxs-lookup"><span data-stu-id="e5365-105">Remarks</span></span>

<span data-ttu-id="e5365-106">**RefreshRecord**アクションは、現在のセット内のレコードに加えられた変更のみを示しています。</span><span class="sxs-lookup"><span data-stu-id="e5365-106">the **RefreshRecord** action shows only changes made to records in the current set.</span></span> <span data-ttu-id="e5365-107">**RefreshRecord**アクションで、データベースが実際に再いないため現在のセット追加されたか、データベースは、最後に再クエリのために削除されたレコードを除外するレコードは含まれません不要になったクエリまたはフィルターの条件を満たすレコードを除外するされます。</span><span class="sxs-lookup"><span data-stu-id="e5365-107">Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter.</span></span> <span data-ttu-id="e5365-108">データベースのクエリを再実行するには、 **[Requery](requery-macro-action.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e5365-108">To requery the database, use the **[Requery](requery-macro-action.md)** method.</span></span> <span data-ttu-id="e5365-109">フォームのレコード ソースをクエリすると、ときに現在のレコードのセットはレコード ソースのすべてのデータを正確に反映します。</span><span class="sxs-lookup"><span data-stu-id="e5365-109">When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="e5365-110">このマクロ アクションの動作は、このマクロ アクションをクライアント データベースで呼び出しているか、または Web データベースで呼び出しているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e5365-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="e5365-111">クライアント データベースの場合</span><span class="sxs-lookup"><span data-stu-id="e5365-111">Client database</span></span>

<span data-ttu-id="e5365-112">クライアント データベースでは、アクティブ フォームまたはアクティブ データシートの現在のセット内のデータに加えられた変更を反映するために基になるレコード ソースを更新するのに**RefreshRecord**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e5365-112">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set.</span></span> <span data-ttu-id="e5365-113">現在のユーザーによって、またはマルチ ユーザー環境で他のユーザーによって加えられた変更も含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5365-113">Changes include those made by the current user or by other users in a multiuser environment.</span></span> <span data-ttu-id="e5365-114">**[Refresh](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** メソッドと同じであります。</span><span class="sxs-lookup"><span data-stu-id="e5365-114">It is equivalent to the **[Refresh](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** method.</span></span>

<span data-ttu-id="e5365-115">**RefreshRecord**マクロ アクションでは、クライアント データベースで、次が行われます。</span><span class="sxs-lookup"><span data-stu-id="e5365-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="e5365-p103">アクティブ フォームまたはアクティブ データシートのレコード ソースを更新し、現在のレコード セットの行に対する変更を反映します。ODBC リンク テーブルについては、現在のレコード セットに対する変更をデータ ソースから取得します。</span><span class="sxs-lookup"><span data-stu-id="e5365-p103">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="e5365-118">現在のレコード セットを更新し、変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="e5365-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="e5365-119">表示に変更される場合は、レコード ソース内の行を削除すると、\#削除します。</span><span class="sxs-lookup"><span data-stu-id="e5365-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="e5365-120">アクティブまたはすべてを表示するデータシートを更新およびレコードの変更\#現在のセット内のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="e5365-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="e5365-121">アクティブ フォームまたはアクティブ データシートのサブフォームおよびサブレポートに再クエリを行います。</span><span class="sxs-lookup"><span data-stu-id="e5365-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="e5365-122">Web データベースの場合</span><span class="sxs-lookup"><span data-stu-id="e5365-122">Web database</span></span>

<span data-ttu-id="e5365-123">Web データベースでは、アクティブ フォームまたはアクティブ データシートの現在のセット内のレコードに加えられた変更を反映するために基になるレコード ソースを更新するのに**RefreshRecord**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e5365-123">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span> <span data-ttu-id="e5365-124">現在のユーザーまたは他のユーザーによって加えられた変更も含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5365-124">Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="e5365-125">**RefreshRecord**マクロ アクションでは、web データベースで、次が行われます。</span><span class="sxs-lookup"><span data-stu-id="e5365-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="e5365-p106">現在のレコード セットのベース テーブルに対する変更を、サーバーから取得します。ODBC リンク テーブルについては、現在のレコード セットに対する変更をデータ ソースから取得します。</span><span class="sxs-lookup"><span data-stu-id="e5365-p106">Retrieves changes from the server for any base tables in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="e5365-128">現在のレコード セットを更新し、変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="e5365-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="e5365-129">表示するのには変更される場合は現在のセット内の行を削除すると、\#削除します。</span><span class="sxs-lookup"><span data-stu-id="e5365-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="e5365-130">更新アクティブなフォームまたはデータシートを表示するのには変更されたレコード、および\#現在のセット内のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="e5365-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="e5365-131">アクティブ フォームまたはアクティブ データシートのサブフォームおよびサブレポートに再クエリを行います。</span><span class="sxs-lookup"><span data-stu-id="e5365-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

