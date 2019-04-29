---
title: PidTagIpmSubtreeEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412731"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="ea81d-103">PidTagIpmSubtreeEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea81d-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ea81d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea81d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea81d-105">メッセージストアのフォルダーツリー内の個人間メッセージ (IPM) フォルダーサブツリーのルートのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="ea81d-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea81d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ea81d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea81d-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ea81d-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ea81d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ea81d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea81d-109">0x35e0</span><span class="sxs-lookup"><span data-stu-id="ea81d-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="ea81d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ea81d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea81d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ea81d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ea81d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ea81d-112">Area:</span></span>  <br/> |<span data-ttu-id="ea81d-113">フォルダー</span><span class="sxs-lookup"><span data-stu-id="ea81d-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea81d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ea81d-114">Remarks</span></span>

<span data-ttu-id="ea81d-115">このプロパティは、IPM 階層のルートを表します。</span><span class="sxs-lookup"><span data-stu-id="ea81d-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="ea81d-116">IPM クライアントは、このプロパティで表されるフォルダーのサブフォルダーではないフォルダーを表示しないようにします。</span><span class="sxs-lookup"><span data-stu-id="ea81d-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea81d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ea81d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ea81d-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ea81d-118">Header files</span></span>

<span data-ttu-id="ea81d-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea81d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea81d-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ea81d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea81d-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ea81d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ea81d-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ea81d-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea81d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea81d-123">See also</span></span>



[<span data-ttu-id="ea81d-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ea81d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea81d-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea81d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea81d-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ea81d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea81d-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ea81d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

