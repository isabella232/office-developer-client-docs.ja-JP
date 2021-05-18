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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330122"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="f7cfc-103">PidTagResponsibility 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7cfc-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="f7cfc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7cfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7cfc-105">一部のトランスポート プロバイダーがメッセージをこの受信者に配信する責任を既に受け入れた場合は TRUE、MAPI スプーラーがこのトランスポート プロバイダーが責任を受け入れる必要があると考える場合は FALSE を含む。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7cfc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f7cfc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7cfc-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="f7cfc-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="f7cfc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f7cfc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7cfc-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="f7cfc-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="f7cfc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f7cfc-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7cfc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f7cfc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f7cfc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f7cfc-112">Area:</span></span>  <br/> |<span data-ttu-id="f7cfc-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="f7cfc-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7cfc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f7cfc-114">Remarks</span></span>

<span data-ttu-id="f7cfc-115">MAPI スプーラーが [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)を介してトランスポート プロバイダーに送信メッセージを表示すると、MAPI スプーラーがトランスポート プロバイダーを担当すると見なすすべての受信者に対してこのプロパティを FALSE に設定し、他のすべての受信者に対して TRUE を設定します。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="f7cfc-116">トランスポート プロバイダーは、FALSE に設定されている受信者 **をPR_RESPONSIBILITYする** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="f7cfc-117">受信者への送信に成功した、または決定的に失敗した後、トランスポート プロバイダーは、ソース メッセージでこのプロパティを TRUE に設定して、その受信者に対する責任を受け入れるかどうかを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="f7cfc-118">受信者を調べた後で、トランスポート プロバイダーが受信者を処理できないか処理しないかを判断した場合、トランスポート プロバイダーは false に設定 **PR_RESPONSIBILITYする必要** があります。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="f7cfc-119">MAPI スプーラーは、その受信者を処理できる別のトランスポート プロバイダーを探します。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="f7cfc-120">MAPI スプーラーは最終的に、トランスポート プロバイダーが責任を受け入れる受信者に対して配信不可のレポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="f7cfc-121">トランスポート プロバイダーがメッセージの配信を試み、失敗した場合は、MAPI にエラーの理由を示す [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを呼び出して、MAPI が配信不能レポートを生成できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7cfc-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f7cfc-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7cfc-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f7cfc-123">Protocol specifications</span></span>

<span data-ttu-id="f7cfc-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7cfc-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7cfc-125">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7cfc-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7cfc-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7cfc-127">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7cfc-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f7cfc-128">Header files</span></span>

<span data-ttu-id="f7cfc-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7cfc-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7cfc-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7cfc-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7cfc-131">Mapitags.h</span></span>
  
> <span data-ttu-id="f7cfc-132">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f7cfc-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7cfc-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7cfc-133">See also</span></span>



[<span data-ttu-id="f7cfc-134">PidTagDeleteAfterSubmit ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="f7cfc-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="f7cfc-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f7cfc-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7cfc-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7cfc-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7cfc-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f7cfc-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7cfc-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f7cfc-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

