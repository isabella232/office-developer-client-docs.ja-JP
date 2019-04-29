---
title: PidTagServiceName 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438961"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="d1d7f-103">PidTagServiceName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1d7f-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="d1d7f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1d7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1d7f-105">mapisvc.inf ファイル内のユーザーによって設定されたメッセージサービスの名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="d1d7f-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1d7f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d1d7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1d7f-107">PR_SERVICE_NAME、PR_SERVICE_NAME_A、PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="d1d7f-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="d1d7f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d1d7f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1d7f-109">0x3d09</span><span class="sxs-lookup"><span data-stu-id="d1d7f-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="d1d7f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d1d7f-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1d7f-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1d7f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d1d7f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d1d7f-112">Area:</span></span>  <br/> |<span data-ttu-id="d1d7f-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="d1d7f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1d7f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d1d7f-114">Remarks</span></span>

<span data-ttu-id="d1d7f-115">これらのプロパティに含まれる名前は、メッセージサービスに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="d1d7f-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="d1d7f-116">これは、mapisvc.inf の [サービス] セクションから取得されます。</span><span class="sxs-lookup"><span data-stu-id="d1d7f-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="d1d7f-117">これらのプロパティは、メッセージサービステーブルの列として表示され、サービスのフィルター処理に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1d7f-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="d1d7f-118">サービスを識別してフィルター処理するために使用されるため、この値はローカライズしないでください。</span><span class="sxs-lookup"><span data-stu-id="d1d7f-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1d7f-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d1d7f-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d1d7f-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d1d7f-120">Header files</span></span>

<span data-ttu-id="d1d7f-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1d7f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1d7f-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1d7f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1d7f-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d1d7f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d1d7f-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1d7f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1d7f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1d7f-125">See also</span></span>



[<span data-ttu-id="d1d7f-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d1d7f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1d7f-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1d7f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1d7f-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d1d7f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1d7f-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d1d7f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

