---
title: ActiveCommand プロパティ (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479082"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="950df-102">ActiveCommand プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="950df-102">ActiveCommand Property (ADO)</span></span>


<span data-ttu-id="950df-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="950df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="950df-104">関連付けられた [Recordset](command-object-ado.md) オブジェクトを作成した [Command](recordset-object-ado.md) オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="950df-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="950df-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="950df-105">Return Value</span></span>

<span data-ttu-id="950df-p101">**Command** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を返します。既定は、Null オブジェクト参照です。</span><span class="sxs-lookup"><span data-stu-id="950df-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="950df-108">解説</span><span class="sxs-lookup"><span data-stu-id="950df-108">Remarks</span></span>

<span data-ttu-id="950df-109">**ActiveCommand** プロパティは、値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="950df-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="950df-110">現在の **Recordset** の作成に **Command** オブジェクトが使用されていない場合は、 **Null** オブジェクト参照が返されます。</span><span class="sxs-lookup"><span data-stu-id="950df-110">If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>

<span data-ttu-id="950df-111">このプロパティは、作成された **Recordset** オブジェクトのみが与えられていて、関連付けられている **Command** オブジェクトを取得したい場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="950df-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

