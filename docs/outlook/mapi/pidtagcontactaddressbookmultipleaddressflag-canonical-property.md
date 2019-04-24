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
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344892"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="a9d35-103">PidTagContactAddressBookMultipleAddressFlag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9d35-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="a9d35-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9d35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9d35-105">プロバイダーが連絡先アイテムごとに複数の電子メールアドレスをサポートしている場合に TRUE となるフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a9d35-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9d35-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a9d35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9d35-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="a9d35-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="a9d35-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a9d35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9d35-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="a9d35-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="a9d35-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a9d35-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9d35-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a9d35-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a9d35-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a9d35-112">Area:</span></span>  <br/> |<span data-ttu-id="a9d35-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="a9d35-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9d35-114">解説</span><span class="sxs-lookup"><span data-stu-id="a9d35-114">Remarks</span></span>

<span data-ttu-id="a9d35-115">このプロパティが TRUE の場合、プロバイダーはメールアドレスのない連絡先を許可しません。</span><span class="sxs-lookup"><span data-stu-id="a9d35-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="a9d35-116">FALSE の場合、プロバイダーは、プライマリ電子メールアドレスがあるかどうかにかかわらず、すべての連絡先を表示します。</span><span class="sxs-lookup"><span data-stu-id="a9d35-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="a9d35-117">優先されるのは、プライマリ電子メールアドレスのみです。</span><span class="sxs-lookup"><span data-stu-id="a9d35-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="a9d35-118">これは連絡先アドレス帳コンテナーのプロパティで、連絡先アドレス帳コンテナーの列になります。</span><span class="sxs-lookup"><span data-stu-id="a9d35-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9d35-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a9d35-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a9d35-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a9d35-120">Header files</span></span>

<span data-ttu-id="a9d35-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9d35-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9d35-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a9d35-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9d35-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a9d35-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a9d35-124">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9d35-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9d35-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9d35-125">See also</span></span>



[<span data-ttu-id="a9d35-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a9d35-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9d35-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9d35-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9d35-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a9d35-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9d35-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a9d35-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

