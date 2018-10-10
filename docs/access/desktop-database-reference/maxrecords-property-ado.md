---
title: MaxRecords プロパティ (ADO)
TOCTitle: MaxRecords Property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8753bf09655371042e97ead083c6849f1736b8b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477737"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="f1f1f-102">MaxRecords プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="f1f1f-102">MaxRecords Property (ADO)</span></span>


<span data-ttu-id="f1f1f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1f1f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f1f1f-104">クエリから [Recordset](recordset-object-ado.md) に返す最大レコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="f1f1f-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f1f1f-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="f1f1f-105">Settings and Return Values</span></span>

<span data-ttu-id="f1f1f-p101">返される最大レコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 (制限なし) です。</span><span class="sxs-lookup"><span data-stu-id="f1f1f-p101">Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f1f-108">解説</span><span class="sxs-lookup"><span data-stu-id="f1f1f-108">Remarks</span></span>

<span data-ttu-id="f1f1f-p102">**MaxRecords** プロパティは、プロバイダーがデータ ソースから返すレコード数を制限するために使用します。このプロパティの既定値は 0 で、プロバイダーが要求されたすべてのレコードを返すことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f1f1f-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="f1f1f-111">**MaxRecords** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="f1f1f-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

