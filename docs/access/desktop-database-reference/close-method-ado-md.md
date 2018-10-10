---
title: Close メソッド (ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39059a684a2a64574fc270f3fbd3797a00f66b96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479390"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="1024d-102">Close メソッド (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="1024d-102">Close Method (ADO MD)</span></span>


<span data-ttu-id="1024d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1024d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1024d-104">開いているセルセットを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1024d-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="1024d-105">構文</span><span class="sxs-lookup"><span data-stu-id="1024d-105">Syntax</span></span>

<span data-ttu-id="1024d-106">*セルセット*。閉じる</span><span class="sxs-lookup"><span data-stu-id="1024d-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="1024d-107">解説</span><span class="sxs-lookup"><span data-stu-id="1024d-107">Remarks</span></span>

<span data-ttu-id="1024d-p101">**Close** メソッドを使用して [Cellset](cellset-object-ado-md.md) オブジェクトを閉じると、関連するすべての [Cell](cell-object-ado-md.md)、[Axis](axis-object-ado-md.md)、[Position](position-object-ado-md.md)、または [Member](member-object-ado-md.md) オブジェクトのデータを含む、関連付けられたデータが解放されます。 **Cellset** を閉じてもメモリからは削除されないため、プロパティの設定を変更したり、後から再び開くことが可能です。オブジェクトをメモリから完全に削除するには、オブジェクト変数を **Nothing** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1024d-p101">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects. Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later. To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="1024d-p102">後から [Open](open-method-ado-md.md) メソッドを呼び出して、同じまたは異なるソース文字列を使用する **Cellset** を再び開くことができます。 **Cellset** オブジェクトが閉じている間に、基になるデータまたはメタデータを参照するプロパティを取得したりメソッドを呼び出したりすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1024d-p102">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string. While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>
