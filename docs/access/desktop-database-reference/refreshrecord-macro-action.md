---
title: RefreshRecord マクロ アクション
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d8682c19686650ab193536658c6b56961f289174
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307080"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="3ca67-102">RefreshRecord マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="3ca67-102">RefreshRecord macro action</span></span>


<span data-ttu-id="3ca67-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ca67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ca67-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span><span class="sxs-lookup"><span data-stu-id="3ca67-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca67-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3ca67-105">Remarks</span></span>

<span data-ttu-id="3ca67-p101">the **RefreshRecord** action shows only changes made to records in the current set. Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter. To requery the database, use the **[Requery](requery-macro-action.md)** method. When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span><span class="sxs-lookup"><span data-stu-id="3ca67-p101">the **RefreshRecord** action shows only changes made to records in the current set. Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter. To requery the database, use the **[Requery](requery-macro-action.md)** method. When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="3ca67-110">このマクロ アクションの動作は、このマクロ アクションをクライアント データベースで呼び出しているか、または Web データベースで呼び出しているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="3ca67-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="3ca67-111">クライアント データベースの場合</span><span class="sxs-lookup"><span data-stu-id="3ca67-111">Client database</span></span>

<span data-ttu-id="3ca67-p102">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set. Changes include those made by the current user or by other users in a multiuser environment. It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span><span class="sxs-lookup"><span data-stu-id="3ca67-p102">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set. Changes include those made by the current user or by other users in a multiuser environment. It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span></span>

<span data-ttu-id="3ca67-115">The **RefreshRecord** macro action does the following in a client database:</span><span class="sxs-lookup"><span data-stu-id="3ca67-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="3ca67-p103">アクティブ フォームまたはアクティブ データシートのレコード ソースを更新し、現在のレコード セットの行に対する変更を反映します。ODBC リンク テーブルについては、現在のレコード セットに対する変更をデータ ソースから取得します。</span><span class="sxs-lookup"><span data-stu-id="3ca67-p103">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="3ca67-118">現在のレコード セットを更新し、変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="3ca67-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="3ca67-119">レコードソースの行が削除されている場合は、[削除済み\#] と表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ca67-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="3ca67-120">アクティブまたはデータシートを更新して、現在の\#セットの変更されたレコードと削除されたレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="3ca67-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="3ca67-121">アクティブ フォームまたはアクティブ データシートのサブフォームおよびサブレポートに再クエリを行います。</span><span class="sxs-lookup"><span data-stu-id="3ca67-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="3ca67-122">Web データベースの場合</span><span class="sxs-lookup"><span data-stu-id="3ca67-122">Web database</span></span>

<span data-ttu-id="3ca67-p105">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set. Changes include those made by the current user or other users.</span><span class="sxs-lookup"><span data-stu-id="3ca67-p105">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set. Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="3ca67-125">The **RefreshRecord** macro action does the following in a web database:</span><span class="sxs-lookup"><span data-stu-id="3ca67-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="3ca67-p106">現在のレコード セットのベース テーブルに対する変更を、サーバーから取得します。ODBC リンク テーブルについては、現在のレコード セットに対する変更をデータ ソースから取得します。</span><span class="sxs-lookup"><span data-stu-id="3ca67-p106">Retrieves changes from the server for any base tables in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="3ca67-128">現在のレコード セットを更新し、変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="3ca67-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="3ca67-129">現在のセットの行が削除されている場合は、[削除\#済み] を表示するように変更されます。</span><span class="sxs-lookup"><span data-stu-id="3ca67-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="3ca67-130">アクティブなフォームまたはデータシートを更新して、現在\#のセットの変更されたレコードと削除されたレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="3ca67-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="3ca67-131">アクティブ フォームまたはアクティブ データシートのサブフォームおよびサブレポートに再クエリを行います。</span><span class="sxs-lookup"><span data-stu-id="3ca67-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

