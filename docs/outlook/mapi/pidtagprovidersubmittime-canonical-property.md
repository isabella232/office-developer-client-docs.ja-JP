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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c5e840250da7ba3b95150f2e83e1eb08b0c61ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409021"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="49cec-103">PidTagProviderSubmitTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49cec-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="49cec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49cec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49cec-105">トランスポート プロバイダーが基になるメッセージング システムにメッセージを渡した日時を格納します。</span><span class="sxs-lookup"><span data-stu-id="49cec-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49cec-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="49cec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49cec-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="49cec-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="49cec-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="49cec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49cec-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="49cec-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="49cec-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="49cec-110">Data type:</span></span>  <br/> |<span data-ttu-id="49cec-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="49cec-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="49cec-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="49cec-112">Area:</span></span>  <br/> |<span data-ttu-id="49cec-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="49cec-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49cec-114">注釈</span><span class="sxs-lookup"><span data-stu-id="49cec-114">Remarks</span></span>

<span data-ttu-id="49cec-115">このプロパティは、メッセージの送信時に送信トランスポート プロバイダーによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="49cec-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="49cec-116">このプロパティは、X.400 送信エンベロープのメッセージごとの属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="49cec-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="49cec-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="49cec-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="49cec-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="49cec-118">Header files</span></span>

<span data-ttu-id="49cec-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49cec-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="49cec-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="49cec-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="49cec-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="49cec-121">Mapitags.h</span></span>
  
> <span data-ttu-id="49cec-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="49cec-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49cec-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="49cec-123">See also</span></span>



[<span data-ttu-id="49cec-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="49cec-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49cec-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49cec-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49cec-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="49cec-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49cec-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="49cec-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

