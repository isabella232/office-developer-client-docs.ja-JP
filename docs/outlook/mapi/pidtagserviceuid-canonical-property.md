---
title: PidTagServiceUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426528"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="f3cf3-103">PidTagServiceUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3cf3-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="f3cf3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3cf3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3cf3-105">メッセージ サービス [の MAPIUID](mapiuid.md) 構造を格納します。</span><span class="sxs-lookup"><span data-stu-id="f3cf3-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3cf3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f3cf3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3cf3-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="f3cf3-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="f3cf3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f3cf3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3cf3-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="f3cf3-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="f3cf3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f3cf3-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3cf3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f3cf3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f3cf3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f3cf3-112">Area:</span></span>  <br/> |<span data-ttu-id="f3cf3-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="f3cf3-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3cf3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f3cf3-114">Remarks</span></span>

<span data-ttu-id="f3cf3-115">このプロパティは、プロファイル セクション オブジェクトの MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="f3cf3-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="f3cf3-116">MAPI は、同じメッセージ サービスに属しているすべてのプロバイダーをグループ化するために使用します。</span><span class="sxs-lookup"><span data-stu-id="f3cf3-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="f3cf3-117">このプロパティは、ほとんどの [IMsgServiceAdmin](imsgserviceadminiunknown.md) メソッドにパラメーターとして指定されます。</span><span class="sxs-lookup"><span data-stu-id="f3cf3-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="f3cf3-118">Mapisvc.inf には表示されません。</span><span class="sxs-lookup"><span data-stu-id="f3cf3-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f3cf3-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f3cf3-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f3cf3-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f3cf3-120">Header files</span></span>

<span data-ttu-id="f3cf3-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3cf3-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3cf3-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f3cf3-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3cf3-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3cf3-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f3cf3-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f3cf3-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3cf3-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3cf3-125">See also</span></span>



[<span data-ttu-id="f3cf3-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3cf3-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="f3cf3-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f3cf3-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3cf3-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3cf3-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3cf3-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f3cf3-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3cf3-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f3cf3-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

