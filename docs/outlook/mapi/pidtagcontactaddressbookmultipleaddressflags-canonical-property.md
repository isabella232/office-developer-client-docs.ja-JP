---
title: PidTagContactAddressBookMultipleAddressFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588672"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="91d0f-103">PidTagContactAddressBookMultipleAddressFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91d0f-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="91d0f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91d0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91d0f-105">連絡先アイテムごとでは、プロバイダーが複数の電子メールをサポートするかどうかを示すフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="91d0f-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91d0f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91d0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91d0f-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="91d0f-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="91d0f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="91d0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91d0f-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="91d0f-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="91d0f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91d0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="91d0f-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="91d0f-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="91d0f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="91d0f-112">Area:</span></span>  <br/> |<span data-ttu-id="91d0f-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="91d0f-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91d0f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="91d0f-114">Remarks</span></span>

<span data-ttu-id="91d0f-115">このプロパティのフラグが TRUE の場合は、プロバイダーでは、この電子メール アドレスがない連絡先は含まれません。</span><span class="sxs-lookup"><span data-stu-id="91d0f-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="91d0f-116">プライマリ電子メール アドレスのみが受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="91d0f-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="91d0f-117">これは、アドレス帳の連絡先のプロファイル セクションのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="91d0f-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91d0f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="91d0f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="91d0f-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="91d0f-119">Header files</span></span>

<span data-ttu-id="91d0f-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91d0f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="91d0f-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="91d0f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="91d0f-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91d0f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="91d0f-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="91d0f-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91d0f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="91d0f-124">See also</span></span>



[<span data-ttu-id="91d0f-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="91d0f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91d0f-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="91d0f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91d0f-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91d0f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91d0f-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91d0f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

