---
title: PidLidSpamOriginalFolder 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4cb0243f38137afa820c3499a8b95954098bd6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802189"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="d53d2-103">PidLidSpamOriginalFolder 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d53d2-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="d53d2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d53d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d53d2-105">その前にメッセージがどのフォルダーが、[迷惑メール] フォルダーにフィルターされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d53d2-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d53d2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d53d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d53d2-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="d53d2-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="d53d2-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d53d2-108">Property set:</span></span>  <br/> |<span data-ttu-id="d53d2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d53d2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d53d2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d53d2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d53d2-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="d53d2-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="d53d2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d53d2-112">Data type:</span></span>  <br/> |<span data-ttu-id="d53d2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d53d2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d53d2-114">領域:</span><span class="sxs-lookup"><span data-stu-id="d53d2-114">Area:</span></span>  <br/> |<span data-ttu-id="d53d2-115">スパム</span><span class="sxs-lookup"><span data-stu-id="d53d2-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d53d2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d53d2-116">Remarks</span></span>

<span data-ttu-id="d53d2-117">このプロパティの値は、移動前にメッセージが含まれているフォルダーの**EntryID**です。</span><span class="sxs-lookup"><span data-stu-id="d53d2-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="d53d2-118">メッセージがスパムとしてマークされている場合、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53d2-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d53d2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d53d2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d53d2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d53d2-120">Protocol specifications</span></span>

<span data-ttu-id="d53d2-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d53d2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d53d2-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d53d2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d53d2-123">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d53d2-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d53d2-124">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="d53d2-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d53d2-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d53d2-125">Header files</span></span>

<span data-ttu-id="d53d2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d53d2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d53d2-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d53d2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d53d2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d53d2-128">See also</span></span>



[<span data-ttu-id="d53d2-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d53d2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d53d2-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d53d2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d53d2-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d53d2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d53d2-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d53d2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

