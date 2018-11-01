---
title: PageCount プロパティ (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef5179f44a2c7c153411ae33566f3806f1e93573
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867371"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="cfa8f-102">PageCount プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="cfa8f-102">PageCount property (ADO)</span></span>


<span data-ttu-id="cfa8f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfa8f-104">[Recordset](recordset-object-ado.md) オブジェクトに含まれるデータのページ数を示します。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="cfa8f-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="cfa8f-105">Return value</span></span>

<span data-ttu-id="cfa8f-106">**Recordset** のページ数を示す長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa8f-107">解説</span><span class="sxs-lookup"><span data-stu-id="cfa8f-107">Remarks</span></span>

<span data-ttu-id="cfa8f-108">**PageCount**プロパティのデータ ページの数を決定するが、**レコード セット**オブジェクトでは使用します。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-108">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="cfa8f-109">*ページ*は、 [PageSize](pagesize-property-ado.md)プロパティの設定のと同じサイズのレコードのグループです。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-109">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="cfa8f-110">**PageSize**の値よりも少ないレコードがあるため、最後のページが完了しない場合でも、 **PageCount**の値に追加ページとしてカウントします。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-110">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="cfa8f-111">**Recordset**オブジェクトがこのプロパティをサポートしていない場合、値は**PageCount**は決められていないことを示す-1 になります。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="cfa8f-112">ページ機能の詳細については、 **PageSize** プロパティおよび [AbsolutePage](absolutepage-property-ado.md) プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfa8f-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

