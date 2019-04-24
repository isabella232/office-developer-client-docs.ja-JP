---
title: PidTagContactAddressBookStoreSupportMasks 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMasks
api_type:
- HeaderDef
ms.assetid: 68f5aac1-714c-48fc-a0cf-a0c0401a6070
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e06d9a3ee2352e05e38ab1f2d86014f970160f9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338263"
---
# <a name="pidtagcontactaddressbookstoresupportmasks-canonical-property"></a><span data-ttu-id="4d438-103">PidTagContactAddressBookStoreSupportMasks 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d438-103">PidTagContactAddressBookStoreSupportMasks Canonical Property</span></span>

  
  
<span data-ttu-id="4d438-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d438-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d438-105">ストアのサポートされている機能を示すフラグを含みます。</span><span class="sxs-lookup"><span data-stu-id="4d438-105">Contains flags indicating the store's supported features.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d438-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4d438-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d438-107">PR_CONTAB_STORE_SUPPORT_MASKS</span><span class="sxs-lookup"><span data-stu-id="4d438-107">PR_CONTAB_STORE_SUPPORT_MASKS</span></span>  <br/> |
|<span data-ttu-id="4d438-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4d438-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d438-109">0x6621</span><span class="sxs-lookup"><span data-stu-id="4d438-109">0x6621</span></span>  <br/> |
|<span data-ttu-id="4d438-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4d438-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d438-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="4d438-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="4d438-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4d438-112">Area:</span></span>  <br/> |<span data-ttu-id="4d438-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="4d438-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d438-114">解説</span><span class="sxs-lookup"><span data-stu-id="4d438-114">Remarks</span></span>

<span data-ttu-id="4d438-115">このプロパティは、連絡先フォルダーを含むストアから取得されます。</span><span class="sxs-lookup"><span data-stu-id="4d438-115">This property is obtained from the stores which contains the Contacts folders.</span></span> <span data-ttu-id="4d438-116">連絡先アドレス帳プロバイダーは、これを使用して、ストアのサポートされている機能の adequacy を評価します。</span><span class="sxs-lookup"><span data-stu-id="4d438-116">The Contact Address Book provider uses it to evaluate the adequacy of the store's supported features.</span></span> <span data-ttu-id="4d438-117">これは、連絡先のアドレス帳の [プロファイル] セクションのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4d438-117">It is a property on a Contact Address Book profile section.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d438-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4d438-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4d438-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4d438-119">Header files</span></span>

<span data-ttu-id="4d438-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d438-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d438-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d438-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d438-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4d438-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4d438-123">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4d438-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d438-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d438-124">See also</span></span>



[<span data-ttu-id="4d438-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4d438-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d438-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d438-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d438-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4d438-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d438-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4d438-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

