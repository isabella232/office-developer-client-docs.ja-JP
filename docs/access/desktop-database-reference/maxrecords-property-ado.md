---
title: MaxRecords プロパティ (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709356"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="0fb7e-102">MaxRecords プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0fb7e-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="0fb7e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0fb7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fb7e-104">クエリから [Recordset](recordset-object-ado.md) に返す最大レコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="0fb7e-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0fb7e-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="0fb7e-105">Settings and return values</span></span>

<span data-ttu-id="0fb7e-p101">返される最大レコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 (制限なし) です。</span><span class="sxs-lookup"><span data-stu-id="0fb7e-p101">Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="0fb7e-108">解説</span><span class="sxs-lookup"><span data-stu-id="0fb7e-108">Remarks</span></span>

<span data-ttu-id="0fb7e-p102">**MaxRecords** プロパティは、プロバイダーがデータ ソースから返すレコード数を制限するために使用します。このプロパティの既定値は 0 で、プロバイダーが要求されたすべてのレコードを返すことを意味します。</span><span class="sxs-lookup"><span data-stu-id="0fb7e-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="0fb7e-111">**MaxRecords** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="0fb7e-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

