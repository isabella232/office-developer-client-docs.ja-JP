---
title: PidTagOriginalSensitivity 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c921d2c9eee69148713408ec2e2a5510a27011a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582708"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="0e9c3-103">PidTagOriginalSensitivity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e9c3-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="0e9c3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e9c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e9c3-105">最初のバージョンのメッセージの送信者によって割り当てられた感度の値が含まれていますは、メッセージを転送または返信する前にします。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e9c3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0e9c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e9c3-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="0e9c3-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="0e9c3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0e9c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e9c3-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="0e9c3-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="0e9c3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0e9c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e9c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e9c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e9c3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0e9c3-112">Area:</span></span>  <br/> |<span data-ttu-id="0e9c3-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="0e9c3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e9c3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0e9c3-114">Remarks</span></span>

<span data-ttu-id="0e9c3-115">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) は、メッセージが最初に送信されると、クライアント アプリケーションは同じ値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="0e9c3-116">後で変更することはありませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="0e9c3-117">このプロパティは、コピーしたエントリの感度を保護するためにトランスポート プロバイダーが使用します。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="0e9c3-118">前方参照または**SENSITIVITY_PRIVATE**としてマークされた元のメッセージに対する返信に元のメッセージ テキストの変更をブロックすることなどのことができます。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e9c3-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0e9c3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e9c3-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0e9c3-120">Protocol specifications</span></span>

<span data-ttu-id="0e9c3-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e9c3-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e9c3-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e9c3-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e9c3-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e9c3-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e9c3-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0e9c3-125">Header files</span></span>

<span data-ttu-id="0e9c3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e9c3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e9c3-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e9c3-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e9c3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0e9c3-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0e9c3-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e9c3-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e9c3-130">See also</span></span>



[<span data-ttu-id="0e9c3-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e9c3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e9c3-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e9c3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e9c3-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e9c3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e9c3-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e9c3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

