---
title: Axes コレクション (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 612a78d8ac99a070f133fd3804f5b69c8093d47c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862602"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="9a167-102">Axes コレクション (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="9a167-102">Axes Collection (ADO MD)</span></span>


<span data-ttu-id="9a167-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a167-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9a167-104">セルセットを定義する [Axis](axis-object-ado-md.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="9a167-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a167-105">解説</span><span class="sxs-lookup"><span data-stu-id="9a167-105">Remarks</span></span>

<span data-ttu-id="9a167-p101">[Cellset](cellset-object-ado-md.md) オブジェクトは、 **Axes** コレクションを含みます。 **Cellset** を開くと、このコレクションには少なくとも 1 つの **Axis** が含まれます。 [Axis](axis-object-ado-md.md) のオブジェクトの使い方の詳細については、 **Axis** オブジェクトを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a167-p101">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection. Once the **Cellset** is opened, this collection will contain at least one **Axis**. See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <span data-ttu-id="9a167-p102">[!メモ] **Cellset** のフィルター軸は、 **Axes** コレクションには含まれません。詳細については、 [FilterAxis](filteraxis-property-ado-md.md) プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a167-p102">The filter axis of a **Cellset** is not contained in the **Axes** collection. See the [FilterAxis](filteraxis-property-ado-md.md) property for more information.</span></span>



<span data-ttu-id="9a167-p103">**Axes** は、標準の ADO コレクションです。このコレクションのプロパティとメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="9a167-p103">**Axes** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="9a167-113">[Count](count-property-ado.md) プロパティを使用して、コレクションのオブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="9a167-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="9a167-114">既定の [Item](item-property-ado.md) プロパティを使用して、コレクションからオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="9a167-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="9a167-115">[Refresh](refresh-method-ado.md) メソッドを使用して、プロバイダーからコレクションのオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="9a167-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

