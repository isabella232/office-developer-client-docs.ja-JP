---
title: PidTagContactAddressBookFolderName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookFolderName
api_type:
- HeaderDef
ms.assetid: 6149da2f-6e42-429c-bcdb-d517d21df720
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d131681ab9a49f1d25d14641855fb19c2456b0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565411"
---
# <a name="pidtagcontactaddressbookfoldername-canonical-property"></a><span data-ttu-id="2dd49-103">PidTagContactAddressBookFolderName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2dd49-103">PidTagContactAddressBookFolderName Canonical Property</span></span>

  
  
<span data-ttu-id="2dd49-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dd49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dd49-105">アドレス帳のエントリに使用されるフォルダーの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2dd49-105">Contains a folder name used for address book entries.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2dd49-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2dd49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2dd49-107">PR_CONTAB_FOLDER_NAME、PR_CONTAB_FOLDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="2dd49-107">PR_CONTAB_FOLDER_NAME, PR_CONTAB_FOLDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="2dd49-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2dd49-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2dd49-109">0x6613</span><span class="sxs-lookup"><span data-stu-id="2dd49-109">0x6613</span></span>  <br/> |
|<span data-ttu-id="2dd49-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2dd49-110">Data type:</span></span>  <br/> |<span data-ttu-id="2dd49-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="2dd49-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="2dd49-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2dd49-112">Area:</span></span>  <br/> |<span data-ttu-id="2dd49-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="2dd49-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dd49-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2dd49-114">Remarks</span></span>

<span data-ttu-id="2dd49-115">フォルダー名には、次の文字を使用できません。</span><span class="sxs-lookup"><span data-stu-id="2dd49-115">The following characters cannot be used in folder names:</span></span>
  
<span data-ttu-id="2dd49-116">[ ] / \ &amp; ~ ?</span><span class="sxs-lookup"><span data-stu-id="2dd49-116">[ ] / \ &amp; ~ ?</span></span> <span data-ttu-id="2dd49-117">\* | \<\> " ; : +</span><span class="sxs-lookup"><span data-stu-id="2dd49-117">\* | \< \> " ; : +</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2dd49-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2dd49-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2dd49-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2dd49-119">Header files</span></span>

<span data-ttu-id="2dd49-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2dd49-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2dd49-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2dd49-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2dd49-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2dd49-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2dd49-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2dd49-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2dd49-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2dd49-124">See also</span></span>



[<span data-ttu-id="2dd49-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2dd49-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2dd49-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2dd49-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2dd49-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2dd49-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2dd49-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2dd49-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

