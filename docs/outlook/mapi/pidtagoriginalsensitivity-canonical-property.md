---
title: PidTagOriginalSensitivity の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6d461c88e96a3f749595b3e071737107480472aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803099"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="c3ef0-103">PidTagOriginalSensitivity の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c3ef0-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="c3ef0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3ef0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3ef0-105">最初のバージョンのメッセージの送信者によって割り当てられた感度の値が含まれていますは、メッセージを転送または返信する前にします。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3ef0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3ef0-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="c3ef0-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="c3ef0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c3ef0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3ef0-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="c3ef0-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="c3ef0-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3ef0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c3ef0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c3ef0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c3ef0-112">Area:</span></span>  <br/> |<span data-ttu-id="c3ef0-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="c3ef0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3ef0-114">備考</span><span class="sxs-lookup"><span data-stu-id="c3ef0-114">Remarks</span></span>

<span data-ttu-id="c3ef0-115">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) は、メッセージが最初に送信されると、クライアント アプリケーションは同じ値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="c3ef0-116">後で変更することはありませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="c3ef0-117">このプロパティは、コピーしたエントリの感度を保護するためにトランスポート プロバイダーが使用します。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="c3ef0-118">前方参照または**SENSITIVITY_PRIVATE**としてマークされた元のメッセージに対する返信に元のメッセージ テキストの変更をブロックすることなどのことができます。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c3ef0-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c3ef0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3ef0-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c3ef0-120">Protocol specifications</span></span>

<span data-ttu-id="c3ef0-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3ef0-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3ef0-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3ef0-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3ef0-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3ef0-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3ef0-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c3ef0-125">Header files</span></span>

<span data-ttu-id="c3ef0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3ef0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3ef0-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3ef0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c3ef0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c3ef0-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3ef0-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3ef0-130">See also</span></span>



[<span data-ttu-id="c3ef0-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3ef0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3ef0-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3ef0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3ef0-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c3ef0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3ef0-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c3ef0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

