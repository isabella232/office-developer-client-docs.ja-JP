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
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335428"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="7c3b7-103">PidTagReportName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c3b7-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="7c3b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c3b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c3b7-105">このメッセージのレポートを取得する受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c3b7-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c3b7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7c3b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c3b7-107">PR_REPORT_NAME、PR_REPORT_NAME_A、PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="7c3b7-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="7c3b7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7c3b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c3b7-109">0x003a</span><span class="sxs-lookup"><span data-stu-id="7c3b7-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="7c3b7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7c3b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c3b7-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c3b7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7c3b7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7c3b7-112">Area:</span></span>  <br/> |<span data-ttu-id="7c3b7-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="7c3b7-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c3b7-114">解説</span><span class="sxs-lookup"><span data-stu-id="7c3b7-114">Remarks</span></span>

<span data-ttu-id="7c3b7-115">これらのプロパティは、送信者がこのメッセージに対して生成されたレポートを受信することを委任した受信者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="7c3b7-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="7c3b7-116">他のユーザーにレポートをルーティングする必要があるクライアントアプリケーションは、メッセージの送信時にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c3b7-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="7c3b7-117">設定されていない場合、レポートはメッセージ送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="7c3b7-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c3b7-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7c3b7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7c3b7-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7c3b7-119">Header files</span></span>

<span data-ttu-id="7c3b7-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c3b7-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c3b7-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c3b7-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c3b7-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7c3b7-122">Mapitags.h</span></span>
  
> <span data-ttu-id="7c3b7-123">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c3b7-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c3b7-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c3b7-124">See also</span></span>



[<span data-ttu-id="7c3b7-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7c3b7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c3b7-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c3b7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c3b7-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c3b7-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c3b7-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c3b7-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

