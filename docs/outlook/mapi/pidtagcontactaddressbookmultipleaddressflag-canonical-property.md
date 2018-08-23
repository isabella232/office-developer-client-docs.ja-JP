---
title: PidTagContactAddressBookMultipleAddressFlag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 34f61f3ef64e5751f9be3df534c4379583447799
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592697"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="31c2b-103">PidTagContactAddressBookMultipleAddressFlag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="31c2b-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="31c2b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31c2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31c2b-105">連絡先アイテムごとに複数の電子メール アドレスをプロバイダーがサポートする場合は TRUE にするフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="31c2b-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31c2b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="31c2b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31c2b-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="31c2b-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="31c2b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="31c2b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31c2b-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="31c2b-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="31c2b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="31c2b-110">Data type:</span></span>  <br/> |<span data-ttu-id="31c2b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="31c2b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="31c2b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="31c2b-112">Area:</span></span>  <br/> |<span data-ttu-id="31c2b-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="31c2b-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31c2b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="31c2b-114">Remarks</span></span>

<span data-ttu-id="31c2b-115">このプロパティが TRUE の場合、プロバイダーは電子メール アドレスがない連絡先を許可しません。</span><span class="sxs-lookup"><span data-stu-id="31c2b-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="31c2b-116">FALSE の場合、プロバイダーは、通常の電子メール アドレスがあるかどうかすべての連絡先を示します。</span><span class="sxs-lookup"><span data-stu-id="31c2b-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="31c2b-117">プライマリ電子メール アドレスのみが受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="31c2b-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="31c2b-118">これは、連絡先のアドレス帳コンテナー、および連絡先のアドレス帳コンテナーのテーブル内の列のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="31c2b-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="31c2b-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="31c2b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="31c2b-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="31c2b-120">Header files</span></span>

<span data-ttu-id="31c2b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31c2b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="31c2b-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="31c2b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="31c2b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31c2b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="31c2b-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31c2b-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31c2b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="31c2b-125">See also</span></span>



[<span data-ttu-id="31c2b-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31c2b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31c2b-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31c2b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31c2b-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="31c2b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31c2b-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="31c2b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

