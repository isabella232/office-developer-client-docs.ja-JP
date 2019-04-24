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
ms.openlocfilehash: 0068b579bb570e49c4403baa017c550814af8f9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357926"
---
# <a name="pidtagcontactaddressbookfoldername-canonical-property"></a><span data-ttu-id="1e63f-103">PidTagContactAddressBookFolderName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e63f-103">PidTagContactAddressBookFolderName Canonical Property</span></span>

  
  
<span data-ttu-id="1e63f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e63f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e63f-105">アドレス帳エントリに使用するフォルダー名を格納します。</span><span class="sxs-lookup"><span data-stu-id="1e63f-105">Contains a folder name used for address book entries.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e63f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1e63f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e63f-107">PR_CONTAB_FOLDER_NAME、PR_CONTAB_FOLDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1e63f-107">PR_CONTAB_FOLDER_NAME, PR_CONTAB_FOLDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="1e63f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1e63f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e63f-109">0x6613</span><span class="sxs-lookup"><span data-stu-id="1e63f-109">0x6613</span></span>  <br/> |
|<span data-ttu-id="1e63f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1e63f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e63f-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="1e63f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="1e63f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1e63f-112">Area:</span></span>  <br/> |<span data-ttu-id="1e63f-113">連絡先のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="1e63f-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e63f-114">解説</span><span class="sxs-lookup"><span data-stu-id="1e63f-114">Remarks</span></span>

<span data-ttu-id="1e63f-115">フォルダー名には次の文字を使用できません。</span><span class="sxs-lookup"><span data-stu-id="1e63f-115">The following characters cannot be used in folder names:</span></span>
  
<span data-ttu-id="1e63f-116">[ ] / \ &amp; ~ ?</span><span class="sxs-lookup"><span data-stu-id="1e63f-116">[ ] / \ &amp; ~ ?</span></span> <span data-ttu-id="1e63f-117">\* | \<\> " ; : +</span><span class="sxs-lookup"><span data-stu-id="1e63f-117">\* | \< \> " ; : +</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e63f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1e63f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1e63f-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1e63f-119">Header files</span></span>

<span data-ttu-id="1e63f-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e63f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e63f-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e63f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e63f-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1e63f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="1e63f-123">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e63f-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e63f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e63f-124">See also</span></span>



[<span data-ttu-id="1e63f-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1e63f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e63f-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e63f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e63f-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1e63f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e63f-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1e63f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

