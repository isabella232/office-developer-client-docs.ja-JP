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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b06ebbe8cb162d77d60cfffa866438567c84c27
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576835"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="d404f-103">PidTagRemoteValidateOk 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d404f-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="d404f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d404f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d404f-105">このプロパティには、 [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを呼び出してリモート ビューアーが許可されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d404f-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d404f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d404f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d404f-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="d404f-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="d404f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d404f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d404f-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="d404f-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="d404f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d404f-110">Data type:</span></span>  <br/> |<span data-ttu-id="d404f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d404f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d404f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d404f-112">Area:</span></span>  <br/> |<span data-ttu-id="d404f-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="d404f-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d404f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d404f-114">Remarks</span></span>

<span data-ttu-id="d404f-115">このプロパティは、状態テーブルに表示される、トランスポートのパフォーマンスをある程度制御を提供しています。</span><span class="sxs-lookup"><span data-stu-id="d404f-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="d404f-116">それにアイドル状態のリモート ビューアーを指示する別の方法として検討できます。</span><span class="sxs-lookup"><span data-stu-id="d404f-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="d404f-117">TRUE に設定されている場合、リモートのビューアーは**IMAPIStatus::ValidateState**を何度でも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d404f-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="d404f-118">FALSE の値は、リモートのビューアーが呼び出しを行うことはできませんを示します。</span><span class="sxs-lookup"><span data-stu-id="d404f-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="d404f-119">トランスポート プロバイダーは、通常このプロパティを設定、動的に追加の呼び出しを無効にするトランスポート プロバイダーが実行する処理のための十分な量を持つ場合に false を指定する値を設定しています。</span><span class="sxs-lookup"><span data-stu-id="d404f-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="d404f-120">トランスポート プロバイダーが終了したら、さらに**IMAPIStatus::ValidateState**の呼び出しを行うクライアント アプリケーションを許可する場合は TRUE に値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d404f-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d404f-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d404f-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d404f-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d404f-122">Header files</span></span>

<span data-ttu-id="d404f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d404f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d404f-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d404f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d404f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d404f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d404f-126">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d404f-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d404f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d404f-127">See also</span></span>



[<span data-ttu-id="d404f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d404f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d404f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d404f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d404f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d404f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d404f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d404f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

