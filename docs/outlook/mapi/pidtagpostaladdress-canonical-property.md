---
title: PidTagPostalAddress の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPostalAddress
api_type:
- COM
ms.assetid: cf400713-3b42-4ee7-9dea-d52b8bf03ac3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1c51e223eabea6fdcae32e99f7c04c7fd797f9ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803167"
---
# <a name="pidtagpostaladdress-canonical-property"></a><span data-ttu-id="14fe1-103">PidTagPostalAddress の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="14fe1-103">PidTagPostalAddress Canonical Property</span></span>

  
  
<span data-ttu-id="14fe1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14fe1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14fe1-105">受信者の郵便番号と住所が含まれています。</span><span class="sxs-lookup"><span data-stu-id="14fe1-105">Contains the recipient's postal address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14fe1-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="14fe1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14fe1-107">PR_POSTAL_ADDRESS、PR_POSTAL_ADDRESS_A、PR_POSTAL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="14fe1-107">PR_POSTAL_ADDRESS, PR_POSTAL_ADDRESS_A, PR_POSTAL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="14fe1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="14fe1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14fe1-109">0x3A15</span><span class="sxs-lookup"><span data-stu-id="14fe1-109">0x3A15</span></span>  <br/> |
|<span data-ttu-id="14fe1-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="14fe1-110">Data type:</span></span>  <br/> |<span data-ttu-id="14fe1-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="14fe1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="14fe1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="14fe1-112">Area:</span></span>  <br/> |<span data-ttu-id="14fe1-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="14fe1-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14fe1-114">備考</span><span class="sxs-lookup"><span data-stu-id="14fe1-114">Remarks</span></span>

<span data-ttu-id="14fe1-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="14fe1-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="14fe1-116">受信者と受信者の組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="14fe1-116">They are defined by the recipient and the recipient's organization.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14fe1-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="14fe1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14fe1-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="14fe1-118">Protocol specifications</span></span>

<span data-ttu-id="14fe1-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14fe1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14fe1-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="14fe1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14fe1-121">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14fe1-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14fe1-122">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="14fe1-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14fe1-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="14fe1-123">Header files</span></span>

<span data-ttu-id="14fe1-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14fe1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="14fe1-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="14fe1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="14fe1-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="14fe1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="14fe1-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="14fe1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14fe1-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="14fe1-128">See also</span></span>



[<span data-ttu-id="14fe1-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="14fe1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14fe1-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="14fe1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14fe1-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="14fe1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14fe1-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="14fe1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

