---
title: ActiveCommand プロパティ (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869562"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="0712a-102">ActiveCommand プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0712a-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="0712a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0712a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0712a-104">関連付けられた [Recordset](command-object-ado.md) オブジェクトを作成した [Command](recordset-object-ado.md) オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="0712a-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="0712a-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="0712a-105">Return value</span></span>

<span data-ttu-id="0712a-p101">**Command** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を返します。既定は、Null オブジェクト参照です。</span><span class="sxs-lookup"><span data-stu-id="0712a-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="0712a-108">解説</span><span class="sxs-lookup"><span data-stu-id="0712a-108">Remarks</span></span>

<span data-ttu-id="0712a-109">**ActiveCommand** プロパティは、値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="0712a-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="0712a-110">以前に現在の**レコード セット**を作成する**コマンド**オブジェクトを使用しない場合は、 **Null**オブジェクト参照が返されます。</span><span class="sxs-lookup"><span data-stu-id="0712a-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="0712a-111">このプロパティは、作成された **Recordset** オブジェクトのみが与えられていて、関連付けられている **Command** オブジェクトを取得したい場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="0712a-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

