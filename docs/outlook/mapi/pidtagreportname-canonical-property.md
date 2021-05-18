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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422314"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="590f1-103">PidTagReportName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="590f1-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="590f1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="590f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="590f1-105">このメッセージのレポートを取得する受信者の表示名を格納します。</span><span class="sxs-lookup"><span data-stu-id="590f1-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="590f1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="590f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="590f1-107">PR_REPORT_NAME、PR_REPORT_NAME_A、PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="590f1-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="590f1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="590f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="590f1-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="590f1-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="590f1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="590f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="590f1-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="590f1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="590f1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="590f1-112">Area:</span></span>  <br/> |<span data-ttu-id="590f1-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="590f1-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="590f1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="590f1-114">Remarks</span></span>

<span data-ttu-id="590f1-115">これらのプロパティは、送信者がこのメッセージに対して生成されたレポートを受信するために委任した受信者のアドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="590f1-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="590f1-116">レポートを別のユーザーにルーティングする必要があるクライアント アプリケーションは、メッセージ送信時にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="590f1-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="590f1-117">設定されていない場合、レポートはメッセージ送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="590f1-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="590f1-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="590f1-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="590f1-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="590f1-119">Header files</span></span>

<span data-ttu-id="590f1-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="590f1-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="590f1-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="590f1-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="590f1-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="590f1-122">Mapitags.h</span></span>
  
> <span data-ttu-id="590f1-123">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="590f1-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="590f1-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="590f1-124">See also</span></span>



[<span data-ttu-id="590f1-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="590f1-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="590f1-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="590f1-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="590f1-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="590f1-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="590f1-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="590f1-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

