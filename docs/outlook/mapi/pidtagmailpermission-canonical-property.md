---
title: PidTagMailPermission 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571193"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="843cc-103">PidTagMailPermission 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="843cc-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="843cc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="843cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="843cc-105">メッセージングのユーザーがメッセージを送信する許可されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="843cc-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="843cc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="843cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="843cc-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="843cc-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="843cc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="843cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="843cc-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="843cc-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="843cc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="843cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="843cc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="843cc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="843cc-112">領域:</span><span class="sxs-lookup"><span data-stu-id="843cc-112">Area:</span></span>  <br/> |<span data-ttu-id="843cc-113">Address</span><span class="sxs-lookup"><span data-stu-id="843cc-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="843cc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="843cc-114">Remarks</span></span>

<span data-ttu-id="843cc-115">このプロパティが設定されていない MAPI により真の価値を持つものとして扱います。</span><span class="sxs-lookup"><span data-stu-id="843cc-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="843cc-116">一部のエントリがいない、メールが有効な企業のディレクトリに false を指定するには、このプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="843cc-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="843cc-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="843cc-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="843cc-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="843cc-118">Header files</span></span>

<span data-ttu-id="843cc-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="843cc-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="843cc-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="843cc-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="843cc-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="843cc-121">Mapitags.h</span></span>
  
> <span data-ttu-id="843cc-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="843cc-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="843cc-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="843cc-123">See also</span></span>



[<span data-ttu-id="843cc-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="843cc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="843cc-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="843cc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="843cc-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="843cc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="843cc-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="843cc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

