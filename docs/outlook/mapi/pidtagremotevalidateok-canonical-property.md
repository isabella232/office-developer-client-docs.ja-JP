---
title: PidTagRemoteValidateOk 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424225"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="61762-103">PidTagRemoteValidateOk 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="61762-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="61762-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61762-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61762-105">リモートビューアーが[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを呼び出すことができる場合、このプロパティには TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61762-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61762-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="61762-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61762-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="61762-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="61762-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="61762-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61762-109">0x3e0d</span><span class="sxs-lookup"><span data-stu-id="61762-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="61762-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="61762-110">Data type:</span></span>  <br/> |<span data-ttu-id="61762-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="61762-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="61762-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="61762-112">Area:</span></span>  <br/> |<span data-ttu-id="61762-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="61762-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61762-114">注釈</span><span class="sxs-lookup"><span data-stu-id="61762-114">Remarks</span></span>

<span data-ttu-id="61762-115">このプロパティは、状態テーブルに表示され、トランスポートパフォーマンスを制御できます。</span><span class="sxs-lookup"><span data-stu-id="61762-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="61762-116">リモート閲覧者をアイドル状態にする別の方法として考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="61762-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="61762-117">TRUE に設定されている場合、リモートビューアーは**imapistatus:: validatestate**を必要な回数だけ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="61762-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="61762-118">値が FALSE の場合は、リモート閲覧者がこれ以上呼び出しを行うことができないことを示します。</span><span class="sxs-lookup"><span data-stu-id="61762-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="61762-119">通常、トランスポートプロバイダーは、このプロパティを FALSE に設定して、トランスポートプロバイダーが実行する処理の量が十分である場合に、追加の呼び出しを無効にします。</span><span class="sxs-lookup"><span data-stu-id="61762-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="61762-120">トランスポートプロバイダーが実行されたら、次に値を TRUE に設定して、クライアントアプリケーションがさらに**imapistatus:: validatestate** calls を行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="61762-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="61762-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="61762-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="61762-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="61762-122">Header files</span></span>

<span data-ttu-id="61762-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61762-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="61762-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="61762-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="61762-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="61762-125">Mapitags.h</span></span>
  
> <span data-ttu-id="61762-126">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61762-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61762-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="61762-127">See also</span></span>



[<span data-ttu-id="61762-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="61762-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61762-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="61762-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61762-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="61762-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61762-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="61762-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

