---
title: PidTagProviderSubmitTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571613"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="dd3ff-103">PidTagProviderSubmitTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dd3ff-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="dd3ff-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd3ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd3ff-105">トランスポート プロバイダーでは、その基になるメッセージング システムにメッセージが渡されるときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dd3ff-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd3ff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dd3ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd3ff-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="dd3ff-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="dd3ff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dd3ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dd3ff-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="dd3ff-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="dd3ff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dd3ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="dd3ff-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="dd3ff-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="dd3ff-112">領域:</span><span class="sxs-lookup"><span data-stu-id="dd3ff-112">Area:</span></span>  <br/> |<span data-ttu-id="dd3ff-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="dd3ff-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd3ff-114">注釈</span><span class="sxs-lookup"><span data-stu-id="dd3ff-114">Remarks</span></span>

<span data-ttu-id="dd3ff-115">このプロパティは、メッセージの送信時に送信トランスポート プロバイダーによって設定が。</span><span class="sxs-lookup"><span data-stu-id="dd3ff-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="dd3ff-116">このプロパティは、X.400 送信エンベロープ メッセージごとの属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="dd3ff-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dd3ff-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dd3ff-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dd3ff-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="dd3ff-118">Header files</span></span>

<span data-ttu-id="dd3ff-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd3ff-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd3ff-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dd3ff-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="dd3ff-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dd3ff-121">Mapitags.h</span></span>
  
> <span data-ttu-id="dd3ff-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dd3ff-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd3ff-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="dd3ff-123">See also</span></span>



[<span data-ttu-id="dd3ff-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dd3ff-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd3ff-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dd3ff-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd3ff-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dd3ff-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd3ff-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dd3ff-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

