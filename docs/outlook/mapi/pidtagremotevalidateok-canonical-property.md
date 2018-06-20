---
title: PidTagRemoteValidateOk の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d8d986554352e05398a843723ee802bb4969e5ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803327"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="8e23c-103">PidTagRemoteValidateOk の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8e23c-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="8e23c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e23c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e23c-105">このプロパティには、 [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを呼び出してリモート ビューアーが許可されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e23c-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e23c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8e23c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e23c-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="8e23c-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="8e23c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8e23c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e23c-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="8e23c-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="8e23c-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8e23c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e23c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8e23c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8e23c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8e23c-112">Area:</span></span>  <br/> |<span data-ttu-id="8e23c-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="8e23c-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e23c-114">備考</span><span class="sxs-lookup"><span data-stu-id="8e23c-114">Remarks</span></span>

<span data-ttu-id="8e23c-115">このプロパティは、状態テーブルに表示される、トランスポートのパフォーマンスをある程度制御を提供しています。</span><span class="sxs-lookup"><span data-stu-id="8e23c-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="8e23c-116">それにアイドル状態のリモート ビューアーを指示する別の方法として検討できます。</span><span class="sxs-lookup"><span data-stu-id="8e23c-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="8e23c-117">TRUE に設定されている場合、リモートのビューアーは**IMAPIStatus::ValidateState**を何度でも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8e23c-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="8e23c-118">FALSE の値は、リモートのビューアーが呼び出しを行うことはできませんを示します。</span><span class="sxs-lookup"><span data-stu-id="8e23c-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="8e23c-119">トランスポート プロバイダーは、通常このプロパティを設定、動的に追加の呼び出しを無効にするトランスポート プロバイダーが実行する処理のための十分な量を持つ場合に false を指定する値を設定しています。</span><span class="sxs-lookup"><span data-stu-id="8e23c-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="8e23c-120">トランスポート プロバイダーが終了したら、さらに**IMAPIStatus::ValidateState**の呼び出しを行うクライアント アプリケーションを許可する場合は TRUE に値を設定します。</span><span class="sxs-lookup"><span data-stu-id="8e23c-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e23c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e23c-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8e23c-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8e23c-122">Header files</span></span>

<span data-ttu-id="8e23c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e23c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e23c-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e23c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e23c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e23c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8e23c-126">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e23c-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e23c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e23c-127">See also</span></span>



[<span data-ttu-id="8e23c-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e23c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e23c-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e23c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e23c-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8e23c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e23c-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8e23c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

