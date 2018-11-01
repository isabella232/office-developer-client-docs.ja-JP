---
title: XML のレコードセットの動的プロパティ
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48714b9178e99cfd4ccf7738f3ad4a342572fdfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884262"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="47ec6-102">XML のレコードセットの動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="47ec6-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="47ec6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="47ec6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="47ec6-104">XML のレコードセットの動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="47ec6-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="47ec6-105">次に挙げる Client Cursor Engine からの、プロバイダー固有の **Recordset** プロパティは、現在 XML 形式で保存されています。</span><span class="sxs-lookup"><span data-stu-id="47ec6-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="47ec6-106">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="47ec6-106">**Update Resync**</span></span>

  - <span data-ttu-id="47ec6-107">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="47ec6-107">**Unique Table**</span></span>

  - <span data-ttu-id="47ec6-108">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="47ec6-108">**Unique Schema**</span></span>

  - <span data-ttu-id="47ec6-109">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="47ec6-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="47ec6-110">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="47ec6-110">**Resync Command**</span></span>

  - <span data-ttu-id="47ec6-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="47ec6-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="47ec6-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="47ec6-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="47ec6-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="47ec6-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="47ec6-114">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="47ec6-114">**BatchSize**</span></span>

  - <span data-ttu-id="47ec6-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="47ec6-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="47ec6-116">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="47ec6-116">**Reshape Name**</span></span>

  - <span data-ttu-id="47ec6-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="47ec6-117">**AutoRecalc**</span></span>

<span data-ttu-id="47ec6-p101">これらのプロパティは、保存される **Recordset** の要素定義の属性として "Schema" セクションに保存されます。これらの属性は、行セット スキーマ名前空間で定義され、プレフィックスが "rs:" であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="47ec6-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

