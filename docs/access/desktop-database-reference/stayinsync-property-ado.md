---
title: StayInSync プロパティ (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308492"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="99bfc-102">StayInSync プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="99bfc-102">StayInSync property (ADO)</span></span>


<span data-ttu-id="99bfc-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="99bfc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99bfc-104">親の行の位置が変更されたときに、基になる子のレコード (つまり、*チャプター*) への参照を変更するかどうかを、階層[Recordset](recordset-object-ado.md)オブジェクト内に示します。</span><span class="sxs-lookup"><span data-stu-id="99bfc-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="99bfc-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="99bfc-105">Settings and return values</span></span>

<span data-ttu-id="99bfc-p101">ブール型 (**Boolean**) の値を設定または取得します。既定値は **True** です。**True** の場合は、親の **Recordset** オブジェクトの行位置が変更されるとチャプターが更新されます。**False** の場合は、親の **Recordset** オブジェクトの行位置が変更されても、チャプターは以前のチャプターのデータを参照し続けます。</span><span class="sxs-lookup"><span data-stu-id="99bfc-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bfc-109">注釈</span><span class="sxs-lookup"><span data-stu-id="99bfc-109">Remarks</span></span>

<span data-ttu-id="99bfc-p102">このプロパティは、[Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) によってサポートされるような階層 Recordset に適用され、子の **Recordset** を取得する前に親の **Recordset** を設定しておく必要があります。このプロパティによって、階層レコードセット内の移動が容易になります。</span><span class="sxs-lookup"><span data-stu-id="99bfc-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

