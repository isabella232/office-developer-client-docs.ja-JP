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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280685"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="3e70c-102">AbsolutePage プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3e70c-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="3e70c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e70c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e70c-104">カレント レコードがあるページを示します。</span><span class="sxs-lookup"><span data-stu-id="3e70c-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3e70c-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="3e70c-105">Settings and return values</span></span>

<span data-ttu-id="3e70c-106">1から[Recordset](recordset-object-ado.md)オブジェクトのページ数 ([PageCount](pagecount-property-ado.md)) までの**長整数型 (Long)** の値を設定するか、または[positionenum](positionenum.md)値の1つを取得します。</span><span class="sxs-lookup"><span data-stu-id="3e70c-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e70c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="3e70c-107">Remarks</span></span>

<span data-ttu-id="3e70c-p101">このプロパティを使用すると、カレント レコードが置かれているページのページ番号を識別できます。このプロパティは、[PageSize](pagesize-property-ado.md) プロパティを使用して、各ページが **PageSize** と等しいレコード数を持つように (ただし最終ページのみ例外で、レコード数が少なくなる場合があります) **Recordset** オブジェクトの行セットの合計カウントを一連のページへと論理的に分割します。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e70c-p101">This property can be used to identify the page number on which the current record is located. It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records). The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="3e70c-111">**AbsolutePage** プロパティを取得または設定する際には、ADO により [AbsolutePosition](absoluteposition-property-ado.md) プロパティと [PageSize](pagesize-property-ado.md) プロパティが以下のように組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e70c-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="3e70c-112">**AbsolutePage** を取得する場合、ADO はまず **AbsolutePosition** の値を取得し、それを **PageSize** で割ります。</span><span class="sxs-lookup"><span data-stu-id="3e70c-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="3e70c-113">**AbsolutePage** を設定する場合、ADO は、 **PageSize** に新しい **AbsolutePage** 値を掛けてからその値に 1 を加えることにより、 **AbsolutePosition** を移動します。</span><span class="sxs-lookup"><span data-stu-id="3e70c-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="3e70c-114">その結果、 **AbsolutePage**が正常に設定された後の**Recordset**内の現在の位置は、そのページの最初のレコードになります。</span><span class="sxs-lookup"><span data-stu-id="3e70c-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="3e70c-p103">**AbsolutePage** は、 **AbsolutePosition** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。このプロパティを設定すると、特定のページの先頭レコードへと移動します。総ページ数は、 **PageCount** プロパティから取得できます。</span><span class="sxs-lookup"><span data-stu-id="3e70c-p103">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

