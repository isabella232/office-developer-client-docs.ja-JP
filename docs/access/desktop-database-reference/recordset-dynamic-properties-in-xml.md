---
title: XML でのレコードセットの動的プロパティ
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36069ec0e8e9020bc70ef1ea72ce25f4461c6487
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946959"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="244cb-102">XML でのレコードセットの動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="244cb-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="244cb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="244cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="244cb-104">次に挙げる Client Cursor Engine からの、プロバイダー固有の **Recordset** プロパティは、現在 XML 形式で保存されています。</span><span class="sxs-lookup"><span data-stu-id="244cb-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="244cb-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="244cb-105">**AutoRecalc**</span></span>
- <span data-ttu-id="244cb-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="244cb-106">**BatchSize**</span></span>
- <span data-ttu-id="244cb-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="244cb-107">**CommandTimeout**</span></span>
- <span data-ttu-id="244cb-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="244cb-108">**IRowsetChange**</span></span>
- <span data-ttu-id="244cb-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="244cb-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="244cb-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="244cb-110">**Reshape Name**</span></span>
- <span data-ttu-id="244cb-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="244cb-111">**Resync Command**</span></span>
- <span data-ttu-id="244cb-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="244cb-112">**Unique Catalog**</span></span>
- <span data-ttu-id="244cb-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="244cb-113">**Unique Schema**</span></span>
- <span data-ttu-id="244cb-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="244cb-114">**Unique Table**</span></span>
- <span data-ttu-id="244cb-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="244cb-115">**Update Resync**</span></span>
- <span data-ttu-id="244cb-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="244cb-116">**UpdateCriteria**</span></span>


<span data-ttu-id="244cb-p101">これらのプロパティは、保存される **Recordset** の要素定義の属性として "Schema" セクションに保存されます。これらの属性は、行セット スキーマ名前空間で定義され、プレフィックスが "rs:" であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="244cb-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="244cb-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="244cb-119">See also</span></span>

- [<span data-ttu-id="244cb-120">ADO の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="244cb-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)