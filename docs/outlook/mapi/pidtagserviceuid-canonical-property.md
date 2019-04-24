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
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359445"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="bb534-103">PidTagServiceUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb534-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="bb534-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb534-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb534-105">メッセージサービスの[MAPIUID](mapiuid.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb534-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb534-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bb534-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb534-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="bb534-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="bb534-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bb534-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb534-109">0x3d0c</span><span class="sxs-lookup"><span data-stu-id="bb534-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="bb534-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bb534-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb534-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb534-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb534-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bb534-112">Area:</span></span>  <br/> |<span data-ttu-id="bb534-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="bb534-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb534-114">解説</span><span class="sxs-lookup"><span data-stu-id="bb534-114">Remarks</span></span>

<span data-ttu-id="bb534-115">このプロパティは、プロファイルセクションオブジェクトの MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="bb534-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="bb534-116">MAPI は、これを使用して、同じメッセージサービスに属するすべてのプロバイダーをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="bb534-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="bb534-117">このプロパティは、ほとんどの[IMsgServiceAdmin](imsgserviceadminiunknown.md)メソッドのパラメーターとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="bb534-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="bb534-118">mapisvc.inf には表示されません。</span><span class="sxs-lookup"><span data-stu-id="bb534-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bb534-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bb534-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bb534-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="bb534-120">Header files</span></span>

<span data-ttu-id="bb534-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb534-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb534-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb534-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb534-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="bb534-123">Mapitags.h</span></span>
  
> <span data-ttu-id="bb534-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb534-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb534-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb534-125">See also</span></span>



[<span data-ttu-id="bb534-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb534-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="bb534-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bb534-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb534-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb534-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb534-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb534-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb534-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb534-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

