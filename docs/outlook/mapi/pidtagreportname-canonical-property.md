---
title: PidTagReportName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569583"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="8f5dc-103">PidTagReportName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f5dc-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="8f5dc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f5dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f5dc-105">このメッセージのレポートを取得する必要があります受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f5dc-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f5dc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8f5dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f5dc-107">PR_REPORT_NAME、PR_REPORT_NAME_A、PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8f5dc-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8f5dc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8f5dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f5dc-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="8f5dc-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="8f5dc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8f5dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f5dc-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8f5dc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8f5dc-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8f5dc-112">Area:</span></span>  <br/> |<span data-ttu-id="8f5dc-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="8f5dc-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f5dc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8f5dc-114">Remarks</span></span>

<span data-ttu-id="8f5dc-115">これらのプロパティでは、このメッセージに対して生成されたすべてのレポートを受信する送信者を委任した受信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8f5dc-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="8f5dc-116">レポートを別のユーザーにルーティングする必要がありますクライアント アプリケーションは、メッセージの送信時にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f5dc-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="8f5dc-117">設定されていない場合、レポートは、メッセージの送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="8f5dc-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f5dc-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8f5dc-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8f5dc-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8f5dc-119">Header files</span></span>

<span data-ttu-id="8f5dc-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f5dc-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f5dc-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8f5dc-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f5dc-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8f5dc-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8f5dc-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f5dc-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f5dc-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f5dc-124">See also</span></span>



[<span data-ttu-id="8f5dc-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f5dc-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f5dc-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f5dc-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f5dc-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8f5dc-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f5dc-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8f5dc-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

