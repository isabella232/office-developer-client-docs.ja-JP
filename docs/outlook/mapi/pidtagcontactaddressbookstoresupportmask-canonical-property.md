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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fb40e2c191056fe164c6a06bfdcf4b8e3d6eb92c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434439"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a><span data-ttu-id="54b3c-103">PidTagContactAddressBookStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="54b3c-103">PidTagContactAddressBookStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="54b3c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54b3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54b3c-105">連絡先フォルダーを **PR_STORE_SUPPORT_MASK** ストアから取得したプロパティ [(PidTagStoreSupportMask)](pidtagcontactaddressbookstoresupportmask-canonical-property.md)プロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="54b3c-105">Contains the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) property obtained from the store that contains the Contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54b3c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="54b3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54b3c-107">PR_CONTAB_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="54b3c-107">PR_CONTAB_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="54b3c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="54b3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54b3c-109">0x6611</span><span class="sxs-lookup"><span data-stu-id="54b3c-109">0x6611</span></span>  <br/> |
|<span data-ttu-id="54b3c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="54b3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="54b3c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="54b3c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="54b3c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="54b3c-112">Area:</span></span>  <br/> |<span data-ttu-id="54b3c-113">連絡先アドレス帳</span><span class="sxs-lookup"><span data-stu-id="54b3c-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54b3c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="54b3c-114">Remarks</span></span>

<span data-ttu-id="54b3c-115">連絡先アドレス帳プロバイダーは、このプロパティを使用して、ストアでサポートされている機能の不備を評価します。</span><span class="sxs-lookup"><span data-stu-id="54b3c-115">The Contact Address Book provider uses this property to evaluate the adequacy of the store's supported features.</span></span> <span data-ttu-id="54b3c-116">これは、連絡先アドレス帳コンテナーのプロパティであり、連絡先アドレス帳コンテナーのテーブル内の列です。</span><span class="sxs-lookup"><span data-stu-id="54b3c-116">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54b3c-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="54b3c-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="54b3c-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="54b3c-118">Header files</span></span>

<span data-ttu-id="54b3c-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54b3c-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="54b3c-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="54b3c-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="54b3c-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54b3c-121">Mapitags.h</span></span>
  
> <span data-ttu-id="54b3c-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="54b3c-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54b3c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="54b3c-123">See also</span></span>



[<span data-ttu-id="54b3c-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="54b3c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54b3c-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="54b3c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54b3c-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="54b3c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54b3c-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="54b3c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

