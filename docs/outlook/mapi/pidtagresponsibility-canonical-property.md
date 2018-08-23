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
ms.openlocfilehash: d2a1c49b29ba08775768fc74861ba36b3c6356fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589379"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="232a6-103">PidTagResponsibility 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="232a6-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="232a6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="232a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="232a6-105">MAPI スプーラーは、このトランスポート プロバイダーが責任を受け入れる必要がありますと見なされる場合は、この受信者、および FALSE にメッセージを配信する責任をいくつかのトランスポート プロバイダーが既に受け入れられて場合は、TRUE を格納します。</span><span class="sxs-lookup"><span data-stu-id="232a6-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="232a6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="232a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="232a6-107">れない</span><span class="sxs-lookup"><span data-stu-id="232a6-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="232a6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="232a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="232a6-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="232a6-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="232a6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="232a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="232a6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="232a6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="232a6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="232a6-112">Area:</span></span>  <br/> |<span data-ttu-id="232a6-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="232a6-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="232a6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="232a6-114">Remarks</span></span>

<span data-ttu-id="232a6-115">FALSE にこのプロパティを設定する MAPI スプーラーを無効と見なされるトランスポート プロバイダー責任、および TRUE すべての受信者のすべての MAPI スプーラーが[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)、によって、トランスポート プロバイダーに送信メッセージを表示するとき他の受信者です。</span><span class="sxs-lookup"><span data-stu-id="232a6-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="232a6-116">トランスポート プロバイダーは必要があります**れない**が FALSE に設定を持つすべての受信者を処理しようとしています。</span><span class="sxs-lookup"><span data-stu-id="232a6-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="232a6-117">正常に送信する、または受信者への送信に失敗して確定した後トランスポート プロバイダーは、送信元のメッセージ受信者の責任を受け入れたことを示すには TRUE にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="232a6-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="232a6-118">受信者を調べると後、は、トランスポート プロバイダーは、できないこと、または処理する必要があります決定したら場合、トランスポート プロバイダーは、必要があります [**れない**に false を指定します。</span><span class="sxs-lookup"><span data-stu-id="232a6-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="232a6-119">MAPI スプーラーは、その受信者を処理できる別のトランスポート プロバイダーを探します。</span><span class="sxs-lookup"><span data-stu-id="232a6-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="232a6-120">MAPI スプーラーは、最終的には対象のトランスポート プロバイダーを負いません責任のいずれかの受信者に配信不能レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="232a6-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="232a6-121">トランスポート プロバイダーは、しようと、メッセージの配信に失敗した場合、MAPI は、配信不能レポートを生成できるように、MAPI への障害の理由を示すために[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="232a6-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="232a6-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="232a6-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="232a6-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="232a6-123">Protocol specifications</span></span>

<span data-ttu-id="232a6-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="232a6-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="232a6-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="232a6-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="232a6-126">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="232a6-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="232a6-127">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="232a6-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="232a6-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="232a6-128">Header files</span></span>

<span data-ttu-id="232a6-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="232a6-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="232a6-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="232a6-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="232a6-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="232a6-131">Mapitags.h</span></span>
  
> <span data-ttu-id="232a6-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="232a6-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="232a6-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="232a6-133">See also</span></span>



[<span data-ttu-id="232a6-134">PidTagDeleteAfterSubmit ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="232a6-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="232a6-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="232a6-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="232a6-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="232a6-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="232a6-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="232a6-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="232a6-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="232a6-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

