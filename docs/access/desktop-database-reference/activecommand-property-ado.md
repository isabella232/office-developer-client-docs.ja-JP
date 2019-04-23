---
title: activecommand プロパティ (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281930"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="c8409-102">activecommand プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="c8409-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="c8409-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8409-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8409-104">関連付けられた [Recordset](command-object-ado.md) オブジェクトを作成した [Command](recordset-object-ado.md) オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="c8409-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8409-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="c8409-105">Return value</span></span>

<span data-ttu-id="c8409-106">**Command** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="c8409-106">Returns a **Variant** that contains a **Command** object.</span></span> <span data-ttu-id="c8409-107">既定は、Null オブジェクト参照です。</span><span class="sxs-lookup"><span data-stu-id="c8409-107">Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8409-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c8409-108">Remarks</span></span>

<span data-ttu-id="c8409-109">**ActiveCommand** プロパティは、値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c8409-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="c8409-110">現在の**Recordset**の作成に**Command**オブジェクトが使用されていなかった場合は、 **Null**オブジェクト参照が返されます。</span><span class="sxs-lookup"><span data-stu-id="c8409-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="c8409-111">このプロパティは、作成された **Recordset** オブジェクトのみが与えられていて、関連付けられている **Command** オブジェクトを取得したい場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="c8409-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

