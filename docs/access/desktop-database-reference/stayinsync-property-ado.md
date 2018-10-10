---
title: StayInSync プロパティ (ADO)
TOCTitle: StayInSync Property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f492b2c3f58084be55eca4787cde486dab29ca67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478151"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="8af05-102">StayInSync プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8af05-102">StayInSync Property (ADO)</span></span>


<span data-ttu-id="8af05-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8af05-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8af05-104">親の行の位置が変更されたときに、基になる子のレコード (つまり、この*章*) への参照が変更されたかどうかを階層[レコード セット](recordset-object-ado.md)オブジェクト内に示します。</span><span class="sxs-lookup"><span data-stu-id="8af05-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8af05-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="8af05-105">Settings and Return Values</span></span>

<span data-ttu-id="8af05-p101">ブール型 ( **Boolean** ) の値を設定または取得します。既定値は **True** です。 **True** の場合は、親の **Recordset** オブジェクトの行位置が変更されるとチャプターが更新されます。 **False** の場合は、親の **Recordset** オブジェクトの行位置が変更されても、チャプターは以前のチャプターのデータを参照し続けます。</span><span class="sxs-lookup"><span data-stu-id="8af05-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af05-109">解説</span><span class="sxs-lookup"><span data-stu-id="8af05-109">Remarks</span></span>

<span data-ttu-id="8af05-p102">このプロパティは、[Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) によってサポートされるような階層 Recordset に適用され、子の **Recordset** を取得する前に親の **Recordset** を設定しておく必要があります。このプロパティによって、階層レコードセット内の移動が容易になります。</span><span class="sxs-lookup"><span data-stu-id="8af05-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

