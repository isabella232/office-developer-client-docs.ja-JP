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
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286440"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="9ba5a-103">PidTagProviderOrdinal 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ba5a-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="9ba5a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ba5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ba5a-105">プロバイダーテーブル内のサービスプロバイダーの位置の0から始まるインデックスを格納します。</span><span class="sxs-lookup"><span data-stu-id="9ba5a-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ba5a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9ba5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ba5a-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="9ba5a-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="9ba5a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9ba5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ba5a-109">0x300d</span><span class="sxs-lookup"><span data-stu-id="9ba5a-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="9ba5a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9ba5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ba5a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9ba5a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9ba5a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9ba5a-112">Area:</span></span>  <br/> |<span data-ttu-id="9ba5a-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="9ba5a-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ba5a-114">解説</span><span class="sxs-lookup"><span data-stu-id="9ba5a-114">Remarks</span></span>

<span data-ttu-id="9ba5a-115">このプロパティは MAPI で計算されます。</span><span class="sxs-lookup"><span data-stu-id="9ba5a-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="9ba5a-116">[IMsgServiceAdmin:: getprovidertable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出して、プロバイダーテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="9ba5a-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="9ba5a-117">このプロパティのプロバイダテーブルを並べ替えて、トランスポート順序を表示します。</span><span class="sxs-lookup"><span data-stu-id="9ba5a-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9ba5a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9ba5a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ba5a-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9ba5a-119">Header files</span></span>

<span data-ttu-id="9ba5a-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ba5a-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ba5a-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9ba5a-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ba5a-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9ba5a-122">Mapitags.h</span></span>
  
> <span data-ttu-id="9ba5a-123">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ba5a-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ba5a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ba5a-124">See also</span></span>



[<span data-ttu-id="9ba5a-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9ba5a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ba5a-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ba5a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ba5a-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9ba5a-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ba5a-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9ba5a-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

