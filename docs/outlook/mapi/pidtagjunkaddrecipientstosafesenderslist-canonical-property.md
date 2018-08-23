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
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802907"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="c2a29-103">PidTagJunkAddRecipientsToSafeSendersList 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c2a29-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="c2a29-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2a29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2a29-105">メール受信者が差出人セーフ リストに追加するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c2a29-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2a29-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c2a29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2a29-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="c2a29-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="c2a29-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c2a29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2a29-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="c2a29-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="c2a29-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c2a29-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2a29-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c2a29-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c2a29-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c2a29-112">Area:</span></span>  <br/> |<span data-ttu-id="c2a29-113">スパム</span><span class="sxs-lookup"><span data-stu-id="c2a29-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2a29-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c2a29-114">Remarks</span></span>

<span data-ttu-id="c2a29-115">存在する場合、このプロパティが 0 または 1 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2a29-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="c2a29-116">1 の値は、メール受信者が差出人セーフ リストに追加することを示します。</span><span class="sxs-lookup"><span data-stu-id="c2a29-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="c2a29-117">0 の値は、メール受信者が差出人セーフ リストに追加されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="c2a29-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="c2a29-118">このプロパティが 1 の値である場合は、迷惑メールのルールの条件の句を差出人セーフ リストに電子メールの受信者の SMTP アドレスを追加しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c2a29-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="c2a29-119">このプロパティが 0 の場合は、操作する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c2a29-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c2a29-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c2a29-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2a29-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c2a29-121">Protocol specifications</span></span>

<span data-ttu-id="c2a29-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2a29-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2a29-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c2a29-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c2a29-124">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2a29-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2a29-125">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="c2a29-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2a29-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c2a29-126">Header files</span></span>

<span data-ttu-id="c2a29-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2a29-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2a29-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c2a29-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2a29-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2a29-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c2a29-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c2a29-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2a29-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2a29-131">See also</span></span>



[<span data-ttu-id="c2a29-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c2a29-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2a29-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c2a29-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2a29-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c2a29-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2a29-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c2a29-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

