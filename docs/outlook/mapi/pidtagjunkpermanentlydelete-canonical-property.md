---
title: PidTagJunkPermanentlyDelete 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkPermanentlyDelete
api_type:
- HeaderDef
ms.assetid: 5f06ad00-7205-48d8-a9ff-f5c6b5e38c5e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c3e766dc494234ed500892cfa2fc8590c347f8e6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393811"
---
# <a name="pidtagjunkpermanentlydelete-canonical-property"></a><span data-ttu-id="9acb4-103">PidTagJunkPermanentlyDelete 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9acb4-103">PidTagJunkPermanentlyDelete Canonical Property</span></span>

  
  
<span data-ttu-id="9acb4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9acb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9acb4-105">スパムを完全に削除することがありますように、メッセージを 1 に設定が確認された場合は、意味します。</span><span class="sxs-lookup"><span data-stu-id="9acb4-105">Signifies, if set to 1, that messages identified as spam may be permanently deleted.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9acb4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9acb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9acb4-107">PR_JUNK_PERMANENTLY_DELETE</span><span class="sxs-lookup"><span data-stu-id="9acb4-107">PR_JUNK_PERMANENTLY_DELETE</span></span>  <br/> |
|<span data-ttu-id="9acb4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9acb4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9acb4-109">0x6102</span><span class="sxs-lookup"><span data-stu-id="9acb4-109">0x6102</span></span>  <br/> |
|<span data-ttu-id="9acb4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9acb4-110">Data type:</span></span>  <br/> |<span data-ttu-id="9acb4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9acb4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9acb4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9acb4-112">Area:</span></span>  <br/> |<span data-ttu-id="9acb4-113">スパム</span><span class="sxs-lookup"><span data-stu-id="9acb4-113">Spam</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9acb4-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9acb4-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9acb4-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9acb4-115">Protocol specifications</span></span>

<span data-ttu-id="9acb4-116">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9acb4-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9acb4-117">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9acb4-117">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9acb4-118">[[MS OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9acb4-118">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9acb4-119">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="9acb4-119">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9acb4-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9acb4-120">Header files</span></span>

<span data-ttu-id="9acb4-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9acb4-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="9acb4-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9acb4-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="9acb4-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9acb4-123">Mapitags.h</span></span>
  
> <span data-ttu-id="9acb4-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9acb4-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9acb4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="9acb4-125">See also</span></span>



[<span data-ttu-id="9acb4-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9acb4-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9acb4-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9acb4-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9acb4-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9acb4-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9acb4-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9acb4-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

