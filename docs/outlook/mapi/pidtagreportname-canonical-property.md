---
title: PidTagReportName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803346"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="3eb75-103">PidTagReportName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3eb75-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="3eb75-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3eb75-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3eb75-105">このメッセージのレポートを取得する必要があります受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3eb75-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3eb75-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3eb75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3eb75-107">PR_REPORT_NAME、PR_REPORT_NAME_A、PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3eb75-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3eb75-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3eb75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3eb75-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="3eb75-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="3eb75-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3eb75-110">Data type:</span></span>  <br/> |<span data-ttu-id="3eb75-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3eb75-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3eb75-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3eb75-112">Area:</span></span>  <br/> |<span data-ttu-id="3eb75-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="3eb75-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eb75-114">備考</span><span class="sxs-lookup"><span data-stu-id="3eb75-114">Remarks</span></span>

<span data-ttu-id="3eb75-115">これらのプロパティでは、このメッセージに対して生成されたすべてのレポートを受信する送信者を委任した受信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="3eb75-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="3eb75-116">レポートを別のユーザーにルーティングする必要がありますクライアント アプリケーションは、メッセージの送信時にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3eb75-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="3eb75-117">設定されていない場合、レポートは、メッセージの送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="3eb75-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3eb75-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3eb75-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3eb75-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3eb75-119">Header files</span></span>

<span data-ttu-id="3eb75-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3eb75-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="3eb75-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3eb75-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="3eb75-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3eb75-122">Mapitags.h</span></span>
  
> <span data-ttu-id="3eb75-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3eb75-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3eb75-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="3eb75-124">See also</span></span>



[<span data-ttu-id="3eb75-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3eb75-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3eb75-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3eb75-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3eb75-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3eb75-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3eb75-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3eb75-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

