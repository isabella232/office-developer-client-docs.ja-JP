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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582253"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="61936-103">PidTagServiceUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="61936-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="61936-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61936-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61936-105">メッセージ サービスの[MAPIUID](mapiuid.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61936-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61936-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="61936-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61936-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="61936-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="61936-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="61936-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61936-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="61936-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="61936-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="61936-110">Data type:</span></span>  <br/> |<span data-ttu-id="61936-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="61936-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="61936-112">領域:</span><span class="sxs-lookup"><span data-stu-id="61936-112">Area:</span></span>  <br/> |<span data-ttu-id="61936-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="61936-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61936-114">注釈</span><span class="sxs-lookup"><span data-stu-id="61936-114">Remarks</span></span>

<span data-ttu-id="61936-115">このプロパティは、プロファイル セクション オブジェクトを MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="61936-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="61936-116">同じメッセージ サービスに属するすべてのプロバイダーをグループ化するのには MAPI を使用します。</span><span class="sxs-lookup"><span data-stu-id="61936-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="61936-117">このプロパティは、ほとんどの[IMsgServiceAdmin](imsgserviceadminiunknown.md)メソッドのパラメーターとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="61936-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="61936-118">Mapisvc.inf には表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61936-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="61936-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="61936-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="61936-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="61936-120">Header files</span></span>

<span data-ttu-id="61936-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61936-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="61936-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="61936-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="61936-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="61936-123">Mapitags.h</span></span>
  
> <span data-ttu-id="61936-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61936-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61936-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="61936-125">See also</span></span>



[<span data-ttu-id="61936-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61936-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="61936-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="61936-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61936-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="61936-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61936-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="61936-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61936-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="61936-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

