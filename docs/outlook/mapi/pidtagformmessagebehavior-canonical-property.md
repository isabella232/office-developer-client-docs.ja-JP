---
title: PidTagFormMessageBehavior 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormMessageBehavior
api_type:
- HeaderDef
ms.assetid: 8fd82432-9fd9-49ed-aa52-72109db04dc9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8bfb7e5af2e2e5e1a51225dc1cf20baf897752c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432885"
---
# <a name="pidtagformmessagebehavior-canonical-property"></a><span data-ttu-id="19f18-103">PidTagFormMessageBehavior 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19f18-103">PidTagFormMessageBehavior Canonical Property</span></span>

  
  
<span data-ttu-id="19f18-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19f18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19f18-105">現在のフォルダーでメッセージを構成する必要がある場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="19f18-105">Contains TRUE if a message should be composed in the current folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19f18-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="19f18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19f18-107">PR_FORM_MESSAGE_BEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="19f18-107">PR_FORM_MESSAGE_BEHAVIOR</span></span>  <br/> |
|<span data-ttu-id="19f18-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="19f18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19f18-109">0x330A</span><span class="sxs-lookup"><span data-stu-id="19f18-109">0x330A</span></span>  <br/> |
|<span data-ttu-id="19f18-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="19f18-110">Data type:</span></span>  <br/> |<span data-ttu-id="19f18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="19f18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="19f18-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="19f18-112">Area:</span></span>  <br/> |<span data-ttu-id="19f18-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="19f18-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19f18-114">注釈</span><span class="sxs-lookup"><span data-stu-id="19f18-114">Remarks</span></span>

<span data-ttu-id="19f18-115">FALSE の値は、メッセージを他の対人メッセージ 、つまり Outbox フォルダーで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19f18-115">A value of FALSE indicates that the message should be composed as any other interpersonal message, that is, in the Outbox folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19f18-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="19f18-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="19f18-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="19f18-117">Header files</span></span>

<span data-ttu-id="19f18-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19f18-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="19f18-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="19f18-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="19f18-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="19f18-120">Mapitags.h</span></span>
  
> <span data-ttu-id="19f18-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="19f18-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19f18-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="19f18-122">See also</span></span>



[<span data-ttu-id="19f18-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="19f18-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19f18-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19f18-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19f18-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="19f18-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19f18-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="19f18-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

