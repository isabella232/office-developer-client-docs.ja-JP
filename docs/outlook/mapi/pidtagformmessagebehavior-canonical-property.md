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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0abb3cba2b72c18a2bc1a43a07130509ba29b56c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580419"
---
# <a name="pidtagformmessagebehavior-canonical-property"></a><span data-ttu-id="2af57-103">PidTagFormMessageBehavior 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2af57-103">PidTagFormMessageBehavior Canonical Property</span></span>

  
  
<span data-ttu-id="2af57-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2af57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2af57-105">TRUE が含まれる場合、メッセージは、現在のフォルダー内で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2af57-105">Contains TRUE if a message should be composed in the current folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2af57-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2af57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2af57-107">PR_FORM_MESSAGE_BEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="2af57-107">PR_FORM_MESSAGE_BEHAVIOR</span></span>  <br/> |
|<span data-ttu-id="2af57-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2af57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2af57-109">0x330A</span><span class="sxs-lookup"><span data-stu-id="2af57-109">0x330A</span></span>  <br/> |
|<span data-ttu-id="2af57-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2af57-110">Data type:</span></span>  <br/> |<span data-ttu-id="2af57-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2af57-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2af57-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2af57-112">Area:</span></span>  <br/> |<span data-ttu-id="2af57-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="2af57-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2af57-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2af57-114">Remarks</span></span>

<span data-ttu-id="2af57-115">FALSE の値は、こと、メッセージする必要がありますで構成されるその他の個人間のメッセージとしては、[送信トレイ] フォルダーにことを示します。</span><span class="sxs-lookup"><span data-stu-id="2af57-115">A value of FALSE indicates that the message should be composed as any other interpersonal message, that is, in the Outbox folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2af57-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2af57-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2af57-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2af57-117">Header files</span></span>

<span data-ttu-id="2af57-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2af57-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="2af57-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2af57-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="2af57-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2af57-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2af57-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2af57-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2af57-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="2af57-122">See also</span></span>



[<span data-ttu-id="2af57-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2af57-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2af57-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2af57-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2af57-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2af57-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2af57-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2af57-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

