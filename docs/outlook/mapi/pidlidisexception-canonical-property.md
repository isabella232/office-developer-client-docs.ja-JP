---
title: PidLidIsException の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5a36cf21a36f83ec252923ddbb137b3b99456927
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802011"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="7fb34-103">PidLidIsException の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7fb34-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="7fb34-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7fb34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7fb34-105">示します (孤立したインスタンスを含む)、例外を表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7fb34-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fb34-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7fb34-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fb34-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="7fb34-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="7fb34-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7fb34-108">Property set:</span></span>  <br/> |<span data-ttu-id="7fb34-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="7fb34-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="7fb34-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7fb34-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7fb34-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="7fb34-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="7fb34-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7fb34-112">Data type:</span></span>  <br/> |<span data-ttu-id="7fb34-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7fb34-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7fb34-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7fb34-114">Area:</span></span>  <br/> |<span data-ttu-id="7fb34-115">会議</span><span class="sxs-lookup"><span data-stu-id="7fb34-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fb34-116">備考</span><span class="sxs-lookup"><span data-stu-id="7fb34-116">Remarks</span></span>

<span data-ttu-id="7fb34-117">FALSE の値を示します定期的または 1 つのインスタンスを表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7fb34-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="7fb34-118">任意のオブジェクトに対してこのプロパティがない場合は、TRUE の値では例外の埋め込みメッセージを除いて FALSE の値を示します。</span><span class="sxs-lookup"><span data-stu-id="7fb34-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7fb34-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7fb34-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fb34-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7fb34-120">Protocol specifications</span></span>

<span data-ttu-id="7fb34-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fb34-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fb34-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7fb34-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7fb34-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fb34-123">[[MS-OXOCAL] ](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fb34-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fb34-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fb34-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7fb34-125">Header files</span></span>

<span data-ttu-id="7fb34-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fb34-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fb34-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7fb34-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fb34-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7fb34-128">See also</span></span>



[<span data-ttu-id="7fb34-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fb34-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fb34-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fb34-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fb34-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7fb34-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fb34-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7fb34-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

