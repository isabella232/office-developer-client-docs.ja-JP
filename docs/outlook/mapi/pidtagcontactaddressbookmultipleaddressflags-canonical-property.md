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
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357933"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="35b54-103">PidTagContactAddressBookMultipleAddressFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35b54-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="35b54-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35b54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35b54-105">プロバイダーが連絡先アイテムごとに複数の電子メールアドレスをサポートするかどうかを示すフラグを含みます。</span><span class="sxs-lookup"><span data-stu-id="35b54-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35b54-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="35b54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35b54-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="35b54-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="35b54-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="35b54-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35b54-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="35b54-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="35b54-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="35b54-110">Data type:</span></span>  <br/> |<span data-ttu-id="35b54-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="35b54-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="35b54-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="35b54-112">Area:</span></span>  <br/> |<span data-ttu-id="35b54-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="35b54-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35b54-114">解説</span><span class="sxs-lookup"><span data-stu-id="35b54-114">Remarks</span></span>

<span data-ttu-id="35b54-115">このプロパティのフラグが TRUE の場合、プロバイダーには電子メールアドレスのない連絡先は含まれません。</span><span class="sxs-lookup"><span data-stu-id="35b54-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="35b54-116">優先されるのは、プライマリ電子メールアドレスのみです。</span><span class="sxs-lookup"><span data-stu-id="35b54-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="35b54-117">これは、連絡先のアドレス帳の [プロファイル] セクションのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="35b54-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35b54-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="35b54-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35b54-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="35b54-119">Header files</span></span>

<span data-ttu-id="35b54-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35b54-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="35b54-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="35b54-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="35b54-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="35b54-122">Mapitags.h</span></span>
  
> <span data-ttu-id="35b54-123">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="35b54-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35b54-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="35b54-124">See also</span></span>



[<span data-ttu-id="35b54-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="35b54-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35b54-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35b54-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35b54-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="35b54-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35b54-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="35b54-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

