---
title: PageSize プロパティ (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288134"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="0e2b7-102">PageSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e2b7-102">PageSize property (ADO)</span></span>


<span data-ttu-id="0e2b7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e2b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e2b7-104">[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="0e2b7-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0e2b7-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="0e2b7-105">Settings and return values</span></span>

<span data-ttu-id="0e2b7-106">1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="0e2b7-106">Sets or returns a **Long** value that indicates how many records are on a page.</span></span> <span data-ttu-id="0e2b7-107">既定値は 10 です。</span><span class="sxs-lookup"><span data-stu-id="0e2b7-107">The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e2b7-108">注釈</span><span class="sxs-lookup"><span data-stu-id="0e2b7-108">Remarks</span></span>

<span data-ttu-id="0e2b7-109">データの論理ページを構成するレコードの数を調べるには、 **PageSize** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e2b7-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="0e2b7-110">ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。</span><span class="sxs-lookup"><span data-stu-id="0e2b7-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="0e2b7-111">これは、web サーバーのシナリオで、ユーザーが一度に特定の数のレコードを表示してデータをページングできるようにする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="0e2b7-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="0e2b7-112">このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e2b7-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

