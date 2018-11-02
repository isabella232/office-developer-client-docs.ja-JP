---
title: Catalog オブジェクト (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b977db2faf07a47c2e9234cec4a7828def5e6188
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926739"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="3f774-102">Catalog オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3f774-102">Catalog object (ADO MD)</span></span>


<span data-ttu-id="3f774-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3f774-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f774-104">多次元データ プロバイダー (MDP) に固有の多次元スキーマ情報 (つまり、キューブおよび基になる次元、階層、レベル、およびメンバー) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f774-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f774-105">解説</span><span class="sxs-lookup"><span data-stu-id="3f774-105">Remarks</span></span>

<span data-ttu-id="3f774-106">**Catalog** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="3f774-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

  - <span data-ttu-id="3f774-107">[ActiveConnection](activeconnection-property-ado-md.md) プロパティを標準の ADO [Connection](connection-object-ado.md) オブジェクトまたは有効な接続文字列に設定して、カタログを開きます。</span><span class="sxs-lookup"><span data-stu-id="3f774-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

  - <span data-ttu-id="3f774-108">**Name** プロパティを使用して、 [Catalog](name-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="3f774-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="3f774-109">[CubeDefs](cubedefs-collection-ado-md.md) コレクションを使用して、キューブに反復処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="3f774-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

