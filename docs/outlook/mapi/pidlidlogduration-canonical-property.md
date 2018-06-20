---
title: PidLidLogDuration の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cc2d52ec183cc336bf126b1fda9a85d41f704f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802037"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="4d231-103">PidLidLogDuration の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4d231-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="4d231-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d231-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d231-105">ジャーナル メッセージの分単位で、期間を表します。</span><span class="sxs-lookup"><span data-stu-id="4d231-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d231-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="4d231-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d231-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="4d231-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="4d231-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d231-108">Property set:</span></span>  <br/> |<span data-ttu-id="4d231-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="4d231-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="4d231-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4d231-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4d231-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="4d231-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="4d231-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="4d231-112">Data type:</span></span>  <br/> |<span data-ttu-id="4d231-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4d231-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4d231-114">領域:</span><span class="sxs-lookup"><span data-stu-id="4d231-114">Area:</span></span>  <br/> |<span data-ttu-id="4d231-115">�W���[�i��</span><span class="sxs-lookup"><span data-stu-id="4d231-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d231-116">備考</span><span class="sxs-lookup"><span data-stu-id="4d231-116">Remarks</span></span>

<span data-ttu-id="4d231-117">(分)、 **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) と**dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) のプロパティの違いをする必要があるアクティビティの期間です。</span><span class="sxs-lookup"><span data-stu-id="4d231-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d231-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4d231-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d231-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4d231-119">Protocol specifications</span></span>

<span data-ttu-id="4d231-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d231-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d231-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d231-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d231-122">[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d231-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d231-123">プロパティとは、仕訳帳の許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4d231-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d231-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4d231-124">Header files</span></span>

<span data-ttu-id="4d231-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d231-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d231-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d231-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d231-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d231-127">See also</span></span>



[<span data-ttu-id="4d231-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d231-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d231-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d231-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d231-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="4d231-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d231-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="4d231-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

