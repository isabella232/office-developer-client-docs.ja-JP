---
title: PidTagJunkAddRecipientsToSafeSendersList 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282369"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="8e602-103">PidTagJunkAddRecipientsToSafeSendersList 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e602-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="8e602-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e602-105">メール受信者を差出人セーフリストに追加するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e602-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e602-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8e602-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e602-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="8e602-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="8e602-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8e602-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e602-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="8e602-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="8e602-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8e602-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e602-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8e602-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8e602-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8e602-112">Area:</span></span>  <br/> |<span data-ttu-id="8e602-113">スパム</span><span class="sxs-lookup"><span data-stu-id="8e602-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e602-114">解説</span><span class="sxs-lookup"><span data-stu-id="8e602-114">Remarks</span></span>

<span data-ttu-id="8e602-115">指定する場合、このプロパティは0または1に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e602-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="8e602-116">値が1の場合は、メール受信者が差出人セーフリストに追加されることを示します。</span><span class="sxs-lookup"><span data-stu-id="8e602-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="8e602-117">値0は、メール受信者が差出人セーフリストに追加されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8e602-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="8e602-118">このプロパティが1の値に設定されている場合は、電子メールの受信者の SMTP アドレスを迷惑メールルールの条件の信頼できる差出人の句に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e602-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="8e602-119">このプロパティが0の場合は、何もする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8e602-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e602-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e602-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e602-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8e602-121">Protocol specifications</span></span>

<span data-ttu-id="8e602-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e602-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e602-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e602-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e602-124">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e602-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e602-125">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8e602-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e602-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8e602-126">Header files</span></span>

<span data-ttu-id="8e602-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e602-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e602-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e602-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e602-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="8e602-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8e602-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e602-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e602-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e602-131">See also</span></span>



[<span data-ttu-id="8e602-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8e602-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e602-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e602-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e602-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e602-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e602-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e602-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

