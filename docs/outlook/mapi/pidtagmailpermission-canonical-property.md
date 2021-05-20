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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430176"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="c5fab-103">PidTagMailPermission 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c5fab-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="c5fab-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5fab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5fab-105">メッセージング ユーザーがメッセージの送受信を許可されている場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="c5fab-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5fab-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c5fab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5fab-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="c5fab-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="c5fab-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c5fab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5fab-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="c5fab-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="c5fab-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c5fab-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5fab-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c5fab-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c5fab-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c5fab-112">Area:</span></span>  <br/> |<span data-ttu-id="c5fab-113">Address</span><span class="sxs-lookup"><span data-stu-id="c5fab-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5fab-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c5fab-114">Remarks</span></span>

<span data-ttu-id="c5fab-115">このプロパティが設定されていない場合、MAPI は TRUE 値を持つプロパティとして扱います。</span><span class="sxs-lookup"><span data-stu-id="c5fab-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="c5fab-116">一部のエントリが電子メールが有効になっていない企業ディレクトリで、このプロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="c5fab-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c5fab-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c5fab-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c5fab-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c5fab-118">Header files</span></span>

<span data-ttu-id="c5fab-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5fab-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5fab-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c5fab-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5fab-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c5fab-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c5fab-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c5fab-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5fab-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5fab-123">See also</span></span>



[<span data-ttu-id="c5fab-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c5fab-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5fab-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c5fab-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5fab-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c5fab-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5fab-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c5fab-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

