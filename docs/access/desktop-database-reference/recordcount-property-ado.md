---
title: RecordCount プロパティ (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41fb9d8bdcb626fefe2e98fe4c1849554a73a6c3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876163"
---
# <a name="recordcount-property-ado"></a><span data-ttu-id="b1e6c-102">RecordCount プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="b1e6c-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="b1e6c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b1e6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1e6c-104">[Recordset](recordset-object-ado.md) オブジェクト内のレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="b1e6c-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1e6c-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="b1e6c-105">Return value</span></span>

<span data-ttu-id="b1e6c-106">**Recordset** のレコード数を示す長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="b1e6c-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1e6c-107">解説</span><span class="sxs-lookup"><span data-stu-id="b1e6c-107">Remarks</span></span>

<span data-ttu-id="b1e6c-p101">**Recordset** オブジェクトに存在するレコード数を調べるには、 **RecordCount** プロパティを使用します。ADO でレコード数を特定できない場合や、プロバイダーやカーソルのタイプが **RecordCount** をサポートしていない場合、このプロパティは -1 を返します。閉じている **Recordset** オブジェクトの **RecordCount** プロパティを取得しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b1e6c-p101">Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="b1e6c-p102">**Recordset** オブジェクトがおよその位置付けまたはブックマークをサポートしている場合、つまり、 **Supports (adApproxPosition)** または **Supports (adBookmark)** がそれぞれ **True** を返す場合、 **Recordset** の値がすべて設定されているかどうかに関係なく、正確なレコード数が返されます。 **Recordset** オブジェクトがおよその位置付けをサポートしていない場合、正確な **RecordCount** の値を返すにはすべてのレコードを取得してカウントする必要があるので、このプロパティが大量のリソースを消費する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b1e6c-p102">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated. If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="b1e6c-p103">レコード数を特定できるかどうかは、 **Recordset** オブジェクトのカーソルのタイプによって異なります。 **RecordCount** プロパティは、前方スクロールのみのカーソルの場合は -1 を返します。静的カーソルまたはキーセット カーソルの場合は実際の数を返します。動的カーソルの場合はデータ ソースに応じて -1 または実際の数を返します。</span><span class="sxs-lookup"><span data-stu-id="b1e6c-p103">The cursor type of the **Recordset** object affects whether the number of records can be determined. The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

