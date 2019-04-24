---
title: PidTagAccount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359781"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="fb192-103">PidTagAccount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb192-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="fb192-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb192-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb192-105">受信者のアカウント名を含みます。</span><span class="sxs-lookup"><span data-stu-id="fb192-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb192-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fb192-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb192-107">PR_ACCOUNT、PR_ACCOUNT_A、PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="fb192-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="fb192-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fb192-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb192-109">0x3a00</span><span class="sxs-lookup"><span data-stu-id="fb192-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="fb192-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fb192-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb192-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb192-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fb192-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fb192-112">Area:</span></span>  <br/> |<span data-ttu-id="fb192-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="fb192-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb192-114">解説</span><span class="sxs-lookup"><span data-stu-id="fb192-114">Remarks</span></span>

<span data-ttu-id="fb192-115">これらのプロパティは、受信者の id とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb192-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="fb192-116">受信者と組織で定義されています。</span><span class="sxs-lookup"><span data-stu-id="fb192-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="fb192-117">通常、これらのプロパティには、受信者の電子メール名 (電子メールアドレスの最後のコンポーネント) が含まれています。これにより、ローカル組織の受信者が一意に識別されます。</span><span class="sxs-lookup"><span data-stu-id="fb192-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="fb192-118">この電子メール名は、特定のメッセージングドメイン内で一意であることを保証された短い名前にするための、x. 識別名に対応しています。</span><span class="sxs-lookup"><span data-stu-id="fb192-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fb192-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fb192-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb192-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fb192-120">Protocol specifications</span></span>

<span data-ttu-id="fb192-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb192-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb192-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb192-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb192-123">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb192-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb192-124">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb192-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="fb192-125">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb192-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb192-126">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb192-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb192-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fb192-127">Header files</span></span>

<span data-ttu-id="fb192-128">mapitags</span><span class="sxs-lookup"><span data-stu-id="fb192-128">mapitags.h</span></span>
  
> <span data-ttu-id="fb192-129">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb192-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="fb192-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb192-130">mapidefs.h</span></span>
  
> <span data-ttu-id="fb192-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb192-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb192-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb192-132">See also</span></span>



[<span data-ttu-id="fb192-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fb192-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="fb192-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb192-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb192-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fb192-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb192-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fb192-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

