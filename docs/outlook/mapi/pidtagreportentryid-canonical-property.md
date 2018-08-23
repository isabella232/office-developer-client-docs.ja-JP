---
title: PidTagReportEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 558a2235f7cb617bf37ccff77ebeec6e4ba77604
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582617"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="52600-103">PidTagReportEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="52600-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="52600-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52600-105">このメッセージのレポートを受信する受信者のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="52600-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52600-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="52600-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52600-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="52600-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="52600-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="52600-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52600-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="52600-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="52600-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="52600-110">Data type:</span></span>  <br/> |<span data-ttu-id="52600-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="52600-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="52600-112">領域:</span><span class="sxs-lookup"><span data-stu-id="52600-112">Area:</span></span>  <br/> |<span data-ttu-id="52600-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="52600-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52600-114">注釈</span><span class="sxs-lookup"><span data-stu-id="52600-114">Remarks</span></span>

<span data-ttu-id="52600-115">このプロパティは、送信者がこのメッセージに対して生成されたすべてのレポートを受信するのには、委任した受信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="52600-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="52600-116">レポートを別のユーザーにルーティングする必要がありますクライアント アプリケーションは、メッセージの送信時にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52600-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="52600-117">設定されていない場合、レポートは、メッセージの送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="52600-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52600-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="52600-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52600-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="52600-119">Protocol specifications</span></span>

<span data-ttu-id="52600-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52600-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52600-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="52600-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52600-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52600-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52600-123">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="52600-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52600-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="52600-124">Header files</span></span>

<span data-ttu-id="52600-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52600-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="52600-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="52600-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="52600-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52600-127">Mapitags.h</span></span>
  
> <span data-ttu-id="52600-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="52600-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52600-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="52600-129">See also</span></span>



[<span data-ttu-id="52600-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="52600-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52600-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="52600-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52600-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="52600-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52600-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="52600-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

