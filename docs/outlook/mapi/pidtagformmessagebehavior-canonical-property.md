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
ms.openlocfilehash: 8bfb7e5af2e2e5e1a51225dc1cf20baf897752c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316213"
---
# <a name="pidtagformmessagebehavior-canonical-property"></a><span data-ttu-id="77420-103">PidTagFormMessageBehavior 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="77420-103">PidTagFormMessageBehavior Canonical Property</span></span>

  
  
<span data-ttu-id="77420-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77420-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77420-105">現在のフォルダー内にメッセージを構成する必要がある場合は、TRUE を指定します。</span><span class="sxs-lookup"><span data-stu-id="77420-105">Contains TRUE if a message should be composed in the current folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77420-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="77420-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77420-107">PR_FORM_MESSAGE_BEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="77420-107">PR_FORM_MESSAGE_BEHAVIOR</span></span>  <br/> |
|<span data-ttu-id="77420-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="77420-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77420-109">0x330A</span><span class="sxs-lookup"><span data-stu-id="77420-109">0x330A</span></span>  <br/> |
|<span data-ttu-id="77420-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="77420-110">Data type:</span></span>  <br/> |<span data-ttu-id="77420-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="77420-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="77420-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="77420-112">Area:</span></span>  <br/> |<span data-ttu-id="77420-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="77420-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77420-114">解説</span><span class="sxs-lookup"><span data-stu-id="77420-114">Remarks</span></span>

<span data-ttu-id="77420-115">値が FALSE の場合、メッセージは、送信トレイフォルダーにある他の個人外のメッセージとして構成する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="77420-115">A value of FALSE indicates that the message should be composed as any other interpersonal message, that is, in the Outbox folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="77420-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="77420-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="77420-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="77420-117">Header files</span></span>

<span data-ttu-id="77420-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77420-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="77420-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="77420-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="77420-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="77420-120">Mapitags.h</span></span>
  
> <span data-ttu-id="77420-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77420-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77420-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="77420-122">See also</span></span>



[<span data-ttu-id="77420-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="77420-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77420-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="77420-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77420-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="77420-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77420-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="77420-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

