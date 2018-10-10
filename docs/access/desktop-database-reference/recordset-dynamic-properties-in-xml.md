---
title: XML のレコードセットの動的プロパティ
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4193220e450c59e7293ed6befa37d8da23801f27
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476543"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="22243-102">XML のレコードセットの動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="22243-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="22243-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="22243-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="22243-104">XML のレコードセットの動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="22243-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="22243-105">次に挙げる Client Cursor Engine からの、プロバイダー固有の **Recordset** プロパティは、現在 XML 形式で保存されています。</span><span class="sxs-lookup"><span data-stu-id="22243-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="22243-106">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="22243-106">**Update Resync**</span></span>

  - <span data-ttu-id="22243-107">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="22243-107">**Unique Table**</span></span>

  - <span data-ttu-id="22243-108">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="22243-108">**Unique Schema**</span></span>

  - <span data-ttu-id="22243-109">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="22243-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="22243-110">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="22243-110">**Resync Command**</span></span>

  - <span data-ttu-id="22243-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="22243-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="22243-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="22243-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="22243-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="22243-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="22243-114">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="22243-114">**BatchSize**</span></span>

  - <span data-ttu-id="22243-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="22243-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="22243-116">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="22243-116">**Reshape Name**</span></span>

  - <span data-ttu-id="22243-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="22243-117">**AutoRecalc**</span></span>

<span data-ttu-id="22243-p101">これらのプロパティは、保存される **Recordset** の要素定義の属性として "Schema" セクションに保存されます。これらの属性は、行セット スキーマ名前空間で定義され、プレフィックスが "rs:" であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="22243-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

