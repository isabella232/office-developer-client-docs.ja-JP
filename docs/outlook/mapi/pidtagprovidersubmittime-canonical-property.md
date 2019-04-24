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
ms.openlocfilehash: c5e840250da7ba3b95150f2e83e1eb08b0c61ab5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286423"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="b5f0b-103">PidTagProviderSubmitTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b5f0b-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="b5f0b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5f0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5f0b-105">トランスポートプロバイダーが、基になるメッセージングシステムにメッセージを渡した日時を格納します。</span><span class="sxs-lookup"><span data-stu-id="b5f0b-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5f0b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b5f0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5f0b-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="b5f0b-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="b5f0b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b5f0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5f0b-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="b5f0b-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="b5f0b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b5f0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5f0b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b5f0b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b5f0b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b5f0b-112">Area:</span></span>  <br/> |<span data-ttu-id="b5f0b-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="b5f0b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5f0b-114">解説</span><span class="sxs-lookup"><span data-stu-id="b5f0b-114">Remarks</span></span>

<span data-ttu-id="b5f0b-115">このプロパティは、メッセージの送信時に、送信トランスポートプロバイダーによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="b5f0b-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="b5f0b-116">このプロパティは、メッセージごとの400送信エンベロープ属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="b5f0b-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b5f0b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b5f0b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b5f0b-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b5f0b-118">Header files</span></span>

<span data-ttu-id="b5f0b-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5f0b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5f0b-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b5f0b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5f0b-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b5f0b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="b5f0b-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5f0b-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5f0b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5f0b-123">See also</span></span>



[<span data-ttu-id="b5f0b-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b5f0b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5f0b-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b5f0b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5f0b-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b5f0b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5f0b-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b5f0b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

