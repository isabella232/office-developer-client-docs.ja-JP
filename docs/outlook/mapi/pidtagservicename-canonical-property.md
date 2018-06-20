---
title: PidTagServiceName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803536"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="dc45f-103">PidTagServiceName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="dc45f-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="dc45f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc45f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc45f-105">MapiSvc.inf ファイルのユーザーによって設定されたメッセージ サービスの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dc45f-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc45f-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="dc45f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc45f-107">PR_SERVICE_NAME、PR_SERVICE_NAME_A、PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="dc45f-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="dc45f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dc45f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc45f-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="dc45f-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="dc45f-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="dc45f-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc45f-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dc45f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dc45f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="dc45f-112">Area:</span></span>  <br/> |<span data-ttu-id="dc45f-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="dc45f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc45f-114">備考</span><span class="sxs-lookup"><span data-stu-id="dc45f-114">Remarks</span></span>

<span data-ttu-id="dc45f-115">これらのプロパティに含まれている名前は、メッセージ サービスに固有です。</span><span class="sxs-lookup"><span data-stu-id="dc45f-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="dc45f-116">MapiSvc.inf の [サービス] セクションからなります。</span><span class="sxs-lookup"><span data-stu-id="dc45f-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="dc45f-117">これらのプロパティは、メッセージ サービス テーブル内の列として表示され、サービスをフィルター処理に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="dc45f-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="dc45f-118">サービスを特定するためには、値をローカライズしない必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc45f-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc45f-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dc45f-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dc45f-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="dc45f-120">Header files</span></span>

<span data-ttu-id="dc45f-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc45f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc45f-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc45f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc45f-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc45f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="dc45f-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dc45f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc45f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc45f-125">See also</span></span>



[<span data-ttu-id="dc45f-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc45f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc45f-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc45f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc45f-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="dc45f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc45f-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="dc45f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

