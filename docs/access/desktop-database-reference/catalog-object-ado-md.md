---
title: Catalog オブジェクト (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296592"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="0d9a3-102">Catalog オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="0d9a3-102">Catalog object (ADO MD)</span></span>


<span data-ttu-id="0d9a3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d9a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d9a3-104">多次元データ プロバイダー (MDP) に固有の多次元スキーマ情報 (つまり、キューブおよび基になる次元、階層、レベル、およびメンバー) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d9a3-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d9a3-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0d9a3-105">Remarks</span></span>

<span data-ttu-id="0d9a3-106">**Catalog** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="0d9a3-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

- <span data-ttu-id="0d9a3-107">[ActiveConnection](activeconnection-property-ado-md.md) プロパティを標準の ADO [Connection](connection-object-ado.md) オブジェクトまたは有効な接続文字列に設定して、カタログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0d9a3-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

- <span data-ttu-id="0d9a3-108">**Name** プロパティを使用して、 [Catalog](name-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="0d9a3-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="0d9a3-109">[CubeDefs](cubedefs-collection-ado-md.md) コレクションを使用して、キューブに反復処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="0d9a3-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

