---
title: PidTagContactAddressBookStoreSupportMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fb40e2c191056fe164c6a06bfdcf4b8e3d6eb92c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283199"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a><span data-ttu-id="efe2f-103">PidTagContactAddressBookStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="efe2f-103">PidTagContactAddressBookStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="efe2f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efe2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efe2f-105">連絡先フォルダーが格納されているストアから取得した**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) プロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="efe2f-105">Contains the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) property obtained from the store that contains the Contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efe2f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="efe2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efe2f-107">PR_CONTAB_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="efe2f-107">PR_CONTAB_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="efe2f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="efe2f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efe2f-109">0x6611</span><span class="sxs-lookup"><span data-stu-id="efe2f-109">0x6611</span></span>  <br/> |
|<span data-ttu-id="efe2f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="efe2f-110">Data type:</span></span>  <br/> |<span data-ttu-id="efe2f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="efe2f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="efe2f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="efe2f-112">Area:</span></span>  <br/> |<span data-ttu-id="efe2f-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="efe2f-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efe2f-114">解説</span><span class="sxs-lookup"><span data-stu-id="efe2f-114">Remarks</span></span>

<span data-ttu-id="efe2f-115">連絡先アドレス帳プロバイダーは、このプロパティを使用して、ストアのサポートされている機能の adequacy を評価します。</span><span class="sxs-lookup"><span data-stu-id="efe2f-115">The Contact Address Book provider uses this property to evaluate the adequacy of the store's supported features.</span></span> <span data-ttu-id="efe2f-116">これは連絡先アドレス帳コンテナーのプロパティで、連絡先アドレス帳コンテナーの列になります。</span><span class="sxs-lookup"><span data-stu-id="efe2f-116">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="efe2f-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="efe2f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="efe2f-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="efe2f-118">Header files</span></span>

<span data-ttu-id="efe2f-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efe2f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="efe2f-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="efe2f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="efe2f-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="efe2f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="efe2f-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="efe2f-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efe2f-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="efe2f-123">See also</span></span>



[<span data-ttu-id="efe2f-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="efe2f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efe2f-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="efe2f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efe2f-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="efe2f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efe2f-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="efe2f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

