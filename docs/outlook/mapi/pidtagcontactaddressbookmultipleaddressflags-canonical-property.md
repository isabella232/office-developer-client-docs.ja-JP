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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429251"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="78e9b-103">PidTagContactAddressBookMultipleAddressFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78e9b-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="78e9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78e9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78e9b-105">プロバイダーが連絡先アイテムごとに複数の電子メール アドレスをサポートするかどうかを示すフラグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="78e9b-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78e9b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="78e9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78e9b-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="78e9b-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="78e9b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="78e9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78e9b-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="78e9b-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="78e9b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="78e9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="78e9b-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="78e9b-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="78e9b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="78e9b-112">Area:</span></span>  <br/> |<span data-ttu-id="78e9b-113">連絡先アドレス帳</span><span class="sxs-lookup"><span data-stu-id="78e9b-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78e9b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="78e9b-114">Remarks</span></span>

<span data-ttu-id="78e9b-115">このプロパティのフラグが TRUE の場合、プロバイダーには電子メール アドレスのない連絡先は含めずに設定されます。</span><span class="sxs-lookup"><span data-stu-id="78e9b-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="78e9b-116">プライマリ 電子メール アドレスだけが受け入れされます。</span><span class="sxs-lookup"><span data-stu-id="78e9b-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="78e9b-117">これは、[連絡先アドレス帳] プロファイル セクションのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="78e9b-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78e9b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="78e9b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="78e9b-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="78e9b-119">Header files</span></span>

<span data-ttu-id="78e9b-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78e9b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="78e9b-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="78e9b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="78e9b-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="78e9b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="78e9b-123">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="78e9b-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78e9b-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="78e9b-124">See also</span></span>



[<span data-ttu-id="78e9b-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="78e9b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78e9b-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78e9b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78e9b-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="78e9b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78e9b-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="78e9b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

