---
title: PidTagResponsibility 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330122"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="3cf6d-103">PidTagResponsibility 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3cf6d-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="3cf6d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cf6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cf6d-105">一部のトランスポートプロバイダーが既にこの受信者へのメッセージの配信を承認している場合は TRUE、このトランスポートプロバイダーが責任を受け入れる必要があることを MAPI スプーラーが考慮している場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cf6d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3cf6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cf6d-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="3cf6d-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="3cf6d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3cf6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3cf6d-109">0x0e0f</span><span class="sxs-lookup"><span data-stu-id="3cf6d-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="3cf6d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3cf6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="3cf6d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3cf6d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3cf6d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3cf6d-112">Area:</span></span>  <br/> |<span data-ttu-id="3cf6d-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="3cf6d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cf6d-114">解説</span><span class="sxs-lookup"><span data-stu-id="3cf6d-114">Remarks</span></span>

<span data-ttu-id="3cf6d-115">mapi スプーラーがトランスポートプロバイダーに送信メッセージを送信すると、 [IXPLogon:: submitmessage](ixplogon-submitmessage.md)を介して、mapi スプーラーが責任を負うすべての受信者に対してこのプロパティが FALSE に設定され、すべてのトランスポートプロバイダーが TRUE に設定されます。その他の受信者。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="3cf6d-116">トランスポートプロバイダーは、 **PR_RESPONSIBILITY**が FALSE に設定されているすべての受信者の処理を試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="3cf6d-117">受信者に送信または conclusively に失敗した後、トランスポートプロバイダーは、送信元のメッセージでこのプロパティを TRUE に設定して、受信者がその受信者に対して承認されたことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="3cf6d-118">受信者を調べた後、トランスポートプロバイダーがそれを処理できないかどうかを判断する場合は、トランスポートプロバイダーは**PR_RESPONSIBILITY**を FALSE に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="3cf6d-119">MAPI スプーラーは、その受信者を処理できる別のトランスポートプロバイダーを検索します。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="3cf6d-120">MAPI スプーラーは、最終的に、トランスポートプロバイダーが責任を受け入れない受信者に対して、配信不能レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="3cf6d-121">トランスポートプロバイダーがメッセージの配信を試行して失敗した場合は、mapi が配信不能レポートを生成できるように、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出してエラーの理由を mapi に示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3cf6d-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3cf6d-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cf6d-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3cf6d-123">Protocol specifications</span></span>

<span data-ttu-id="3cf6d-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cf6d-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cf6d-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cf6d-126">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cf6d-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cf6d-127">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cf6d-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3cf6d-128">Header files</span></span>

<span data-ttu-id="3cf6d-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cf6d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cf6d-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="3cf6d-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="3cf6d-131">Mapitags.h</span></span>
  
> <span data-ttu-id="3cf6d-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3cf6d-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cf6d-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="3cf6d-133">See also</span></span>



[<span data-ttu-id="3cf6d-134">PidTagDeleteAfterSubmit ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="3cf6d-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="3cf6d-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3cf6d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cf6d-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3cf6d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cf6d-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3cf6d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cf6d-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3cf6d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

