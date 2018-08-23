---
title: PidTagTnefUnprocessedProps 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c25888353857f9233ba487661f5f27d64cd678cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577430"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a><span data-ttu-id="b5ca5-103">PidTagTnefUnprocessedProps 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b5ca5-103">PidTagTnefUnprocessedProps Canonical Property</span></span>

  
  
<span data-ttu-id="b5ca5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5ca5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5ca5-105">トランスポート ニュートラル カプセル化形式 (TNEF) をフィルター処理する場合は、プロパティをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="b5ca5-105">Serializes properties when filtering Transport Neutral Encapsulation Format (TNEF).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5ca5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b5ca5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5ca5-107">PR_TNEF_UNPROCESSED_PROPS</span><span class="sxs-lookup"><span data-stu-id="b5ca5-107">PR_TNEF_UNPROCESSED_PROPS</span></span>  <br/> |
|<span data-ttu-id="b5ca5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b5ca5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5ca5-109">0x0E9C</span><span class="sxs-lookup"><span data-stu-id="b5ca5-109">0x0E9C</span></span>  <br/> |
|<span data-ttu-id="b5ca5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b5ca5-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5ca5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b5ca5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b5ca5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b5ca5-112">Area:</span></span>  <br/> |<span data-ttu-id="b5ca5-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="b5ca5-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5ca5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b5ca5-114">Remarks</span></span>

<span data-ttu-id="b5ca5-115">TNEF が名前付きのプロパティ ストア内に作成することはできませんが含まれている場合に元の TNEF を保存するために、Microsoft Outlook と Outlook Web Access (OWA) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5ca5-115">Used by Microsoft Outlook and Outlook Web Access (OWA) for saving the original TNEF in cases where the TNEF contains named properties that cannot be created in the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5ca5-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b5ca5-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b5ca5-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b5ca5-117">Header files</span></span>

<span data-ttu-id="b5ca5-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5ca5-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5ca5-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b5ca5-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5ca5-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b5ca5-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b5ca5-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5ca5-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5ca5-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5ca5-122">See also</span></span>



[<span data-ttu-id="b5ca5-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b5ca5-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5ca5-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b5ca5-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5ca5-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b5ca5-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5ca5-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b5ca5-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

