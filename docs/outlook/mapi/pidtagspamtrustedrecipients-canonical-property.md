---
title: PidTagSpamTrustedRecipients 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59f43316-3ff6-4ed0-bc29-b31039192b08
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 521bdb280776be28d3526471888834bbd7da0b9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359452"
---
# <a name="pidtagspamtrustedrecipients-canonical-property"></a><span data-ttu-id="84e4b-103">PidTagSpamTrustedRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="84e4b-103">PidTagSpamTrustedRecipients Canonical Property</span></span>
 
<span data-ttu-id="84e4b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84e4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84e4b-105">信頼できる受信者を表す、セミコロンで区切られた電子メールアドレスとドメインのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="84e4b-105">Contains a semicolon-delimited list of email addresses and domains that represent the trusted recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84e4b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="84e4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84e4b-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span><span class="sxs-lookup"><span data-stu-id="84e4b-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span></span>  <br/> |
|<span data-ttu-id="84e4b-108">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="84e4b-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="84e4b-109">0x0419</span><span class="sxs-lookup"><span data-stu-id="84e4b-109">0x0419</span></span>  <br/> |
|<span data-ttu-id="84e4b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="84e4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="84e4b-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84e4b-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="84e4b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="84e4b-112">Area:</span></span>  <br/> |<span data-ttu-id="84e4b-113">スパム</span><span class="sxs-lookup"><span data-stu-id="84e4b-113">Spam</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="84e4b-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="84e4b-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84e4b-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="84e4b-115">Protocol specifications</span></span>

<span data-ttu-id="84e4b-116">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84e4b-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84e4b-117">プロパティセットの定義と、関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="84e4b-117">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84e4b-118">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84e4b-118">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84e4b-119">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="84e4b-119">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84e4b-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="84e4b-120">Header files</span></span>

<span data-ttu-id="84e4b-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84e4b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="84e4b-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="84e4b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="84e4b-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="84e4b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="84e4b-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84e4b-124">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84e4b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="84e4b-125">See also</span></span>

- [<span data-ttu-id="84e4b-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="84e4b-126">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="84e4b-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="84e4b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)  
- [<span data-ttu-id="84e4b-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="84e4b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)  
- [<span data-ttu-id="84e4b-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="84e4b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

