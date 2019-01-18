---
title: XML でのレコードセットの動的プロパティ
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712835"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="ba085-102">XML でのレコードセットの動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba085-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="ba085-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ba085-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba085-104">次に挙げる Client Cursor Engine からの、プロバイダー固有の **Recordset** プロパティは、現在 XML 形式で保存されています。</span><span class="sxs-lookup"><span data-stu-id="ba085-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="ba085-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="ba085-105">**AutoRecalc**</span></span>
- <span data-ttu-id="ba085-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="ba085-106">**BatchSize**</span></span>
- <span data-ttu-id="ba085-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="ba085-107">**CommandTimeout**</span></span>
- <span data-ttu-id="ba085-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="ba085-108">**IRowsetChange**</span></span>
- <span data-ttu-id="ba085-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="ba085-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="ba085-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="ba085-110">**Reshape Name**</span></span>
- <span data-ttu-id="ba085-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="ba085-111">**Resync Command**</span></span>
- <span data-ttu-id="ba085-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="ba085-112">**Unique Catalog**</span></span>
- <span data-ttu-id="ba085-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="ba085-113">**Unique Schema**</span></span>
- <span data-ttu-id="ba085-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="ba085-114">**Unique Table**</span></span>
- <span data-ttu-id="ba085-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="ba085-115">**Update Resync**</span></span>
- <span data-ttu-id="ba085-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="ba085-116">**UpdateCriteria**</span></span>


<span data-ttu-id="ba085-p101">これらのプロパティは、保存される **Recordset** の要素定義の属性として "Schema" セクションに保存されます。これらの属性は、行セット スキーマ名前空間で定義され、プレフィックスが "rs:" であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="ba085-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="ba085-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba085-119">See also</span></span>

- [<span data-ttu-id="ba085-120">ADO の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba085-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)
