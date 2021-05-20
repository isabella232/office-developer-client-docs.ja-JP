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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438352"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="9daee-103">PidTagProviderOrdinal 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9daee-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="9daee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9daee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9daee-105">プロバイダー テーブル内のサービス プロバイダーの位置の 0 から始るインデックスを格納します。</span><span class="sxs-lookup"><span data-stu-id="9daee-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9daee-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9daee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9daee-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="9daee-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="9daee-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9daee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9daee-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="9daee-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="9daee-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9daee-110">Data type:</span></span>  <br/> |<span data-ttu-id="9daee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9daee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9daee-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9daee-112">Area:</span></span>  <br/> |<span data-ttu-id="9daee-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="9daee-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9daee-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9daee-114">Remarks</span></span>

<span data-ttu-id="9daee-115">このプロパティは MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="9daee-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="9daee-116">[IMsgServiceAdmin::GetProviderTable メソッドを](imsgserviceadmin-getprovidertable.md)呼び出して、プロバイダー テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="9daee-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="9daee-117">このプロパティのプロバイダー テーブルを並べ替え、トランスポートの順序を表示します。</span><span class="sxs-lookup"><span data-stu-id="9daee-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9daee-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9daee-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9daee-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9daee-119">Header files</span></span>

<span data-ttu-id="9daee-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9daee-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="9daee-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9daee-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="9daee-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9daee-122">Mapitags.h</span></span>
  
> <span data-ttu-id="9daee-123">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9daee-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9daee-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="9daee-124">See also</span></span>



[<span data-ttu-id="9daee-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9daee-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9daee-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9daee-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9daee-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9daee-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9daee-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9daee-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

