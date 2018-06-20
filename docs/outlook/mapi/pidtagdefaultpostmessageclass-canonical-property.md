---
title: PidTagDefaultPostMessageClass の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 538cc7cdc6dcb281beead6d06ff8644c534ed569
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802648"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="121a0-103">PidTagDefaultPostMessageClass の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="121a0-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="121a0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="121a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="121a0-105">カスタム フォームのメッセージ クラスの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="121a0-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="121a0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="121a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="121a0-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="121a0-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="121a0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="121a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="121a0-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="121a0-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="121a0-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="121a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="121a0-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="121a0-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="121a0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="121a0-112">Area:</span></span>  <br/> |<span data-ttu-id="121a0-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="121a0-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="121a0-114">備考</span><span class="sxs-lookup"><span data-stu-id="121a0-114">Remarks</span></span>

<span data-ttu-id="121a0-115">値がいずれかを指定する必要がある場合は、フォルダーでこのプロパティを設定すると、正確に、ベース メッセージ クラス (たとえば、"IPM.連絡先 [連絡先フォルダーまたは"IPM.予定] の予定表フォルダー)、または、ベース メッセージ クラス (たとえば、"IPM.Contact.MyContact」)。</span><span class="sxs-lookup"><span data-stu-id="121a0-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="121a0-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="121a0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="121a0-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="121a0-117">Protocol specifications</span></span>

<span data-ttu-id="121a0-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="121a0-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="121a0-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="121a0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="121a0-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="121a0-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="121a0-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="121a0-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="121a0-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="121a0-122">Header files</span></span>

<span data-ttu-id="121a0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="121a0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="121a0-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="121a0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="121a0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="121a0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="121a0-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="121a0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="121a0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="121a0-127">See also</span></span>



[<span data-ttu-id="121a0-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="121a0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="121a0-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="121a0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="121a0-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="121a0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="121a0-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="121a0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

