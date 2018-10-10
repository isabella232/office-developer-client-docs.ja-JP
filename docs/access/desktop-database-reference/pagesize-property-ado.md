---
title: PageSize プロパティ (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476606"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="34bc0-102">PageSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="34bc0-102">PageSize Property (ADO)</span></span>


<span data-ttu-id="34bc0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="34bc0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34bc0-104">[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="34bc0-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="34bc0-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="34bc0-105">Settings and Return Values</span></span>

<span data-ttu-id="34bc0-p101">1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 10 です。</span><span class="sxs-lookup"><span data-stu-id="34bc0-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="34bc0-108">解説</span><span class="sxs-lookup"><span data-stu-id="34bc0-108">Remarks</span></span>

<span data-ttu-id="34bc0-p102">データの論理ページを構成するレコード数を調べるには、 **PageSize** プロパティを使用します。ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。これは、Web サーバーで、ユーザーが一度に特定の数のレコードを表示しながら、データのページ間を移動できるようにする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="34bc0-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page. This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="34bc0-112">このプロパティはいつでも設定でき、特定のページの最初のレコードの位置を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="34bc0-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

