---
title: AbsolutePage プロパティ (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705261"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="99057-102">AbsolutePage プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="99057-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="99057-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="99057-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99057-104">カレント レコードがあるページを示します。</span><span class="sxs-lookup"><span data-stu-id="99057-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="99057-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="99057-105">Settings and return values</span></span>

<span data-ttu-id="99057-106">設定 ([PageCount](pagecount-property-ado.md))、[レコード セット](recordset-object-ado.md)オブジェクト内のページの数を 1 から**long 型**の値を返します。 または[PositionEnum](positionenum.md)値のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="99057-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="99057-107">解説</span><span class="sxs-lookup"><span data-stu-id="99057-107">Remarks</span></span>

<span data-ttu-id="99057-p101">このプロパティを使用すると、カレント レコードが置かれているページのページ番号を識別できます。このプロパティは、[PageSize](pagesize-property-ado.md) プロパティを使用して、各ページが **PageSize** と等しいレコード数を持つように (ただし最終ページのみ例外で、レコード数が少なくなる場合があります) **Recordset** オブジェクトの行セットの合計カウントを一連のページへと論理的に分割します。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="99057-p101">This property can be used to identify the page number on which the current record is located. It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records). The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="99057-111">**AbsolutePage** プロパティを取得または設定する際には、ADO により [AbsolutePosition](absoluteposition-property-ado.md) プロパティと [PageSize](pagesize-property-ado.md) プロパティが以下のように組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="99057-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="99057-112">**AbsolutePage** を取得する場合、ADO はまず **AbsolutePosition** の値を取得し、それを **PageSize** で割ります。</span><span class="sxs-lookup"><span data-stu-id="99057-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="99057-113">**AbsolutePage** を設定する場合、ADO は、 **PageSize** に新しい **AbsolutePage** 値を掛けてからその値に 1 を加えることにより、 **AbsolutePosition** を移動します。</span><span class="sxs-lookup"><span data-stu-id="99057-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="99057-114">その結果**と、AbsolutePage**を正常に設定した後、**レコード セット**内の現在位置は、そのページの最初のレコードです。</span><span class="sxs-lookup"><span data-stu-id="99057-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="99057-p103">**AbsolutePage** は、 **AbsolutePosition** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。このプロパティを設定すると、特定のページの先頭レコードへと移動します。総ページ数は、 **PageCount** プロパティから取得できます。</span><span class="sxs-lookup"><span data-stu-id="99057-p103">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

