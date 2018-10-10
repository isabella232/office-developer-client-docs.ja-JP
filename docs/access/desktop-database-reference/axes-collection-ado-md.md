---
title: Axes コレクション (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2b078f2d8f1ea6562d6f82f90943923c7d92a07
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478742"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="7bbec-102">Axes コレクション (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7bbec-102">Axes Collection (ADO MD)</span></span>


<span data-ttu-id="7bbec-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bbec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7bbec-104">セルセットを定義する [Axis](axis-object-ado-md.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="7bbec-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bbec-105">解説</span><span class="sxs-lookup"><span data-stu-id="7bbec-105">Remarks</span></span>

<span data-ttu-id="7bbec-p101">[Cellset](cellset-object-ado-md.md) オブジェクトは、 **Axes** コレクションを含みます。 **Cellset** を開くと、このコレクションには少なくとも 1 つの **Axis** が含まれます。 [Axis](axis-object-ado-md.md) のオブジェクトの使い方の詳細については、 **Axis** オブジェクトを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bbec-p101">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection. Once the **Cellset** is opened, this collection will contain at least one **Axis**. See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7bbec-p102">[!メモ] <STRONG>Cellset</STRONG> のフィルター軸は、 <STRONG>Axes</STRONG> コレクションには含まれません。詳細については、 <A href="filteraxis-property-ado-md.md">FilterAxis</A> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bbec-p102">The filter axis of a <STRONG>Cellset</STRONG> is not contained in the <STRONG>Axes</STRONG> collection. See the <A href="filteraxis-property-ado-md.md">FilterAxis</A> property for more information.</span></span></P>



<span data-ttu-id="7bbec-p103">**Axes** は、標準の ADO コレクションです。このコレクションのプロパティとメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="7bbec-p103">**Axes** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="7bbec-113">[Count](count-property-ado.md) プロパティを使用して、コレクションのオブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="7bbec-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="7bbec-114">既定の [Item](item-property-ado.md) プロパティを使用して、コレクションからオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="7bbec-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="7bbec-115">[Refresh](refresh-method-ado.md) メソッドを使用して、プロバイダーからコレクションのオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="7bbec-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

