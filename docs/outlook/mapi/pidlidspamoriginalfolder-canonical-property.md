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
ms.openlocfilehash: 639d5e96eb56fb543d6a6026b1c9400631cee819
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593341"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="ac760-103">PidLidSpamOriginalFolder 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac760-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="ac760-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac760-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac760-105">その前にメッセージがどのフォルダーが、[迷惑メール] フォルダーにフィルターされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ac760-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac760-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ac760-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac760-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="ac760-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="ac760-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ac760-108">Property set:</span></span>  <br/> |<span data-ttu-id="ac760-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ac760-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ac760-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ac760-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ac760-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="ac760-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="ac760-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ac760-112">Data type:</span></span>  <br/> |<span data-ttu-id="ac760-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ac760-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ac760-114">領域:</span><span class="sxs-lookup"><span data-stu-id="ac760-114">Area:</span></span>  <br/> |<span data-ttu-id="ac760-115">スパム</span><span class="sxs-lookup"><span data-stu-id="ac760-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac760-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ac760-116">Remarks</span></span>

<span data-ttu-id="ac760-117">このプロパティの値は、移動前にメッセージが含まれているフォルダーの**EntryID**です。</span><span class="sxs-lookup"><span data-stu-id="ac760-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="ac760-118">メッセージがスパムとしてマークされている場合、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac760-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac760-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ac760-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac760-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ac760-120">Protocol specifications</span></span>

<span data-ttu-id="ac760-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac760-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac760-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac760-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac760-123">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac760-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac760-124">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="ac760-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac760-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ac760-125">Header files</span></span>

<span data-ttu-id="ac760-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac760-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac760-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac760-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac760-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac760-128">See also</span></span>



[<span data-ttu-id="ac760-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac760-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac760-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac760-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac760-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac760-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac760-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac760-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

