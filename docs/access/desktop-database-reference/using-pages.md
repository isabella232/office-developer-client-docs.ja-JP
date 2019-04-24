---
title: ページを使用する (Access デスクトップデータベースリファレンス)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92d6185c3234a58ea9a84310291d0c37e0272535
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305874"
---
# <a name="using-pages"></a><span data-ttu-id="99b45-102">ページの使用</span><span class="sxs-lookup"><span data-stu-id="99b45-102">Using pages</span></span>


<span data-ttu-id="99b45-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="99b45-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99b45-104">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span><span class="sxs-lookup"><span data-stu-id="99b45-104">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="99b45-105">*ページ*は、 **PageSize**プロパティの設定値に等しいサイズを持つレコードのグループです。</span><span class="sxs-lookup"><span data-stu-id="99b45-105">*Pages* are groups of records whose size equals the **PageSize** property setting.</span></span> <span data-ttu-id="99b45-106">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span><span class="sxs-lookup"><span data-stu-id="99b45-106">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="99b45-107">If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span><span class="sxs-lookup"><span data-stu-id="99b45-107">If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="99b45-p102">データの論理ページを構成するレコードの数を調べるには、 **PageSize** プロパティを使用します。ページ サイズを設定すると、 **AbsolutePage** プロパティを使用して、特定のページの最初のレコードに移動できます。これは、Web サーバー上で、ユーザーが一度に一定の数のレコードを表示し、ページを移動できるようにする場合などに便利です。</span><span class="sxs-lookup"><span data-stu-id="99b45-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the **AbsolutePage** property to move to the first record of a particular page. This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="99b45-111">このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="99b45-111">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

<span data-ttu-id="99b45-p103">現在のレコードが置かれているページ番号を確認するには、 **AbsolutePage** プロパティを使用します。ただし、このプロパティを使用するには、プロバイダーで該当する機能がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="99b45-p103">Use the **AbsolutePage** property to identify the page number on which the current record is located. Again, the provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="99b45-p104">**AbsolutePage** は 1 から始まり、現在のレコードが **Recordset** 内の最初のレコードの場合は、値が 1 になります。特定のページの最初のレコードに移動するには、このプロパティを設定します。ページ数の合計は、 **PageCount** プロパティから取得します。</span><span class="sxs-lookup"><span data-stu-id="99b45-p104">**AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

