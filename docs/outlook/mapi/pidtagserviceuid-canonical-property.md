---
title: PidTagServiceUid の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803553"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="b6635-103">PidTagServiceUid の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b6635-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="b6635-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6635-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6635-105">メッセージ サービスの[MAPIUID](mapiuid.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6635-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6635-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b6635-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6635-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="b6635-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="b6635-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b6635-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6635-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="b6635-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="b6635-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b6635-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6635-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b6635-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b6635-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b6635-112">Area:</span></span>  <br/> |<span data-ttu-id="b6635-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="b6635-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6635-114">備考</span><span class="sxs-lookup"><span data-stu-id="b6635-114">Remarks</span></span>

<span data-ttu-id="b6635-115">このプロパティは、プロファイル セクション オブジェクトを MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="b6635-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="b6635-116">同じメッセージ サービスに属するすべてのプロバイダーをグループ化するのには MAPI を使用します。</span><span class="sxs-lookup"><span data-stu-id="b6635-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="b6635-117">このプロパティは、ほとんどの[IMsgServiceAdmin](imsgserviceadminiunknown.md)メソッドのパラメーターとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="b6635-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="b6635-118">Mapisvc.inf には表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6635-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b6635-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b6635-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b6635-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b6635-120">Header files</span></span>

<span data-ttu-id="b6635-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6635-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6635-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b6635-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6635-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6635-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b6635-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6635-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6635-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6635-125">See also</span></span>



[<span data-ttu-id="b6635-126">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6635-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="b6635-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6635-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6635-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6635-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6635-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b6635-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6635-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b6635-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

