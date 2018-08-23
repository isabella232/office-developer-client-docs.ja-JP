---
title: PidTagProviderOrdinal 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b56ee557884e12728c98827f9eb1a280d7a29c30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803220"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="411ff-103">PidTagProviderOrdinal 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="411ff-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="411ff-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="411ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="411ff-105">プロバイダー テーブル内のサービス プロバイダーの位置の 0 から始まるインデックスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="411ff-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="411ff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="411ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="411ff-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="411ff-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="411ff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="411ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="411ff-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="411ff-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="411ff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="411ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="411ff-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="411ff-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="411ff-112">領域:</span><span class="sxs-lookup"><span data-stu-id="411ff-112">Area:</span></span>  <br/> |<span data-ttu-id="411ff-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="411ff-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="411ff-114">注釈</span><span class="sxs-lookup"><span data-stu-id="411ff-114">Remarks</span></span>

<span data-ttu-id="411ff-115">このプロパティは、MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="411ff-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="411ff-116">プロバイダー テーブルを取得するには、 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="411ff-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="411ff-117">トランスポートの順番を表示するには、このプロパティのプロバイダー テーブルを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="411ff-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="411ff-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="411ff-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="411ff-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="411ff-119">Header files</span></span>

<span data-ttu-id="411ff-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="411ff-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="411ff-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="411ff-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="411ff-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="411ff-122">Mapitags.h</span></span>
  
> <span data-ttu-id="411ff-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="411ff-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="411ff-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="411ff-124">See also</span></span>



[<span data-ttu-id="411ff-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="411ff-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="411ff-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="411ff-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="411ff-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="411ff-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="411ff-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="411ff-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

