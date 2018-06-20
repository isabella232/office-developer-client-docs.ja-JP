---
title: PidTagTnefUnprocessedProps の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ee05f2e539d379e8fe197161fa0f6453add31afb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803638"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a><span data-ttu-id="afc71-103">PidTagTnefUnprocessedProps の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="afc71-103">PidTagTnefUnprocessedProps Canonical Property</span></span>

  
  
<span data-ttu-id="afc71-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="afc71-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="afc71-105">トランスポート ニュートラル カプセル化形式 (TNEF) をフィルター処理する場合は、プロパティをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="afc71-105">Serializes properties when filtering Transport Neutral Encapsulation Format (TNEF).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="afc71-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="afc71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afc71-107">PR_TNEF_UNPROCESSED_PROPS</span><span class="sxs-lookup"><span data-stu-id="afc71-107">PR_TNEF_UNPROCESSED_PROPS</span></span>  <br/> |
|<span data-ttu-id="afc71-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="afc71-108">Identifier:</span></span>  <br/> |<span data-ttu-id="afc71-109">0x0E9C</span><span class="sxs-lookup"><span data-stu-id="afc71-109">0x0E9C</span></span>  <br/> |
|<span data-ttu-id="afc71-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="afc71-110">Data type:</span></span>  <br/> |<span data-ttu-id="afc71-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="afc71-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="afc71-112">領域:</span><span class="sxs-lookup"><span data-stu-id="afc71-112">Area:</span></span>  <br/> |<span data-ttu-id="afc71-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="afc71-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afc71-114">備考</span><span class="sxs-lookup"><span data-stu-id="afc71-114">Remarks</span></span>

<span data-ttu-id="afc71-115">TNEF が名前付きのプロパティ ストア内に作成することはできませんが含まれている場合に元の TNEF を保存するために、Microsoft Outlook と Outlook Web Access (OWA) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="afc71-115">Used by Microsoft Outlook and Outlook Web Access (OWA) for saving the original TNEF in cases where the TNEF contains named properties that cannot be created in the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="afc71-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="afc71-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="afc71-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="afc71-117">Header files</span></span>

<span data-ttu-id="afc71-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="afc71-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="afc71-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="afc71-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="afc71-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="afc71-120">Mapitags.h</span></span>
  
> <span data-ttu-id="afc71-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="afc71-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afc71-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="afc71-122">See also</span></span>



[<span data-ttu-id="afc71-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="afc71-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afc71-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="afc71-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afc71-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="afc71-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afc71-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="afc71-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

