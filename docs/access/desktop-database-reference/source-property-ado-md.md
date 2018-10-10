---
title: Source プロパティ (ADO MD)
TOCTitle: Source Property (ADO MD)
ms:assetid: 956e8bf4-a1af-3202-b289-61073a14ee6c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249664(v=office.15)
ms:contentKeyID: 48546431
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cdd41cd37d009413d39cb9a2223bb5646a4240ce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478352"
---
# <a name="source-property-ado-md"></a><span data-ttu-id="3c099-102">Source プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3c099-102">Source Property (ADO MD)</span></span>


<span data-ttu-id="3c099-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c099-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3c099-104">セルセットのデータ ソースを示します。</span><span class="sxs-lookup"><span data-stu-id="3c099-104">Indicates the source for the data in the cellset.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3c099-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="3c099-105">Settings and Return Values</span></span>

<span data-ttu-id="3c099-p101">バリアント型 ( **Variant** ) の値を設定または取得します。閉じている [Cellset](cellset-object-ado-md.md) オブジェクトに対しては、値の設定と取得が可能です。開いている **Cellset** オブジェクトに対しては、値の取得のみが可能です。このバリアント型 ( **Variant** ) には、たとえば MDX クエリのような、有効な文字列型 ( **String** ) の値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c099-p101">Sets or returns a **Variant**, and is read/write for closed [Cellset](cellset-object-ado-md.md) objects and read-only for open **Cellset** objects. The **Variant** should contain a valid **String**, for example, an MDX query.</span></span>

