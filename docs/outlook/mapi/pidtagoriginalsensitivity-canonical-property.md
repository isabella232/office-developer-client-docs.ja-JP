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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341231"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="c8353-103">PidTagOriginalSensitivity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8353-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="c8353-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8353-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8353-105">メッセージの最初のバージョンの送信者によって割り当てられた、転送または返信される前のメッセージが含まれる。</span><span class="sxs-lookup"><span data-stu-id="c8353-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8353-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c8353-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8353-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="c8353-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="c8353-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c8353-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8353-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="c8353-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="c8353-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c8353-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8353-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c8353-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c8353-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c8353-112">Area:</span></span>  <br/> |<span data-ttu-id="c8353-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="c8353-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8353-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c8353-114">Remarks</span></span>

<span data-ttu-id="c8353-115">クライアント アプリケーションは、メッセージが最初に送信された時点で、PR_SENSITIVITY **(** [PidTagSensitivity](pidtagsensitivity-canonical-property.md)) プロパティと同じ値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8353-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="c8353-116">後で変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c8353-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="c8353-117">このプロパティは、コピーされたエントリの感度を保護するためにトランスポート プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="c8353-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="c8353-118">たとえば、元のメッセージ テキストの変更を、メッセージの転送または返信でブロックしたり、元のメッセージ に対してマークされたメッセージに返信したり **SENSITIVITY_PRIVATE。**</span><span class="sxs-lookup"><span data-stu-id="c8353-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8353-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c8353-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8353-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c8353-120">Protocol specifications</span></span>

<span data-ttu-id="c8353-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8353-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8353-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c8353-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8353-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8353-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8353-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8353-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8353-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c8353-125">Header files</span></span>

<span data-ttu-id="c8353-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8353-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8353-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c8353-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8353-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8353-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c8353-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c8353-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8353-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8353-130">See also</span></span>



[<span data-ttu-id="c8353-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c8353-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8353-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8353-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8353-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8353-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8353-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8353-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

