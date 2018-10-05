---
title: PidTagIpmDraftsEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmDraftsEntryId
api_type:
- HeaderDef
ms.assetid: 17d64211-6265-41f4-b016-3677d75af966
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e259c86803147d782469c8d86b23694d8b54e69d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386398"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a><span data-ttu-id="33c71-103">PidTagIpmDraftsEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="33c71-103">PidTagIpmDraftsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="33c71-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33c71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33c71-105">Outlook の [下書き] フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="33c71-105">Contains the **EntryID** of the Outlook Drafts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33c71-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="33c71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33c71-107">PR_IPM_DRAFTS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="33c71-107">PR_IPM_DRAFTS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="33c71-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="33c71-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33c71-109">0x36D7</span><span class="sxs-lookup"><span data-stu-id="33c71-109">0x36D7</span></span>  <br/> |
|<span data-ttu-id="33c71-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="33c71-110">Data type:</span></span>  <br/> |<span data-ttu-id="33c71-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="33c71-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="33c71-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="33c71-112">Area:</span></span>  <br/> |<span data-ttu-id="33c71-113">Folder</span><span class="sxs-lookup"><span data-stu-id="33c71-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33c71-114">備考</span><span class="sxs-lookup"><span data-stu-id="33c71-114">Remarks</span></span>

<span data-ttu-id="33c71-115">このプロパティは、メッセージ ・ ストアのルート フォルダーと同様に、[受信トレイ] フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="33c71-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="33c71-116">特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="33c71-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="33c71-117">最初に、受信トレイ フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="33c71-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="33c71-118">[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用すると、受信トレイ フォルダーの**エントリ Id**への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="33c71-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="33c71-119">**IMsgStore::GetReceiveFolder**が成功した場合は、受信トレイを開き、 **IMAPIFolder**オブジェクトへの参照を取得する、受信トレイと[IMsgStore::OpenEntry](imsgstore-openentry.md)の**エントリ Id**への参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="33c71-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="33c71-120">**IMsgStore::OpenEntry**が成功した場合は、目的のプロパティを取得する**IMAPIFolder**オブジェクトと[IMAPIProp::GetProps](imapiprop-getprops.md)に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="33c71-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="33c71-121">1、2、または 3 の手順が失敗した場合は、ルート フォルダーのプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="33c71-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="33c71-122">そのためには、 **IMsgStore::OpenEntry**、 **lpEntryID**のメッセージ ・ ストアのルート フォルダーを開き、 **IMAPIFolder**オブジェクトへの参照を取得するのには NULL を指定するを使用します。</span><span class="sxs-lookup"><span data-stu-id="33c71-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="33c71-123">ルート フォルダーを開くときに成功した場合は、目的のプロパティを取得するのには、 **IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="33c71-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="33c71-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="33c71-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33c71-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="33c71-125">Protocol specifications</span></span>

<span data-ttu-id="33c71-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c71-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c71-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="33c71-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33c71-128">[[MS OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c71-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c71-129">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="33c71-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33c71-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="33c71-130">Header files</span></span>

<span data-ttu-id="33c71-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33c71-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="33c71-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="33c71-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="33c71-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33c71-133">Mapitags.h</span></span>
  
> <span data-ttu-id="33c71-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="33c71-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33c71-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="33c71-135">See also</span></span>



[<span data-ttu-id="33c71-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="33c71-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33c71-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="33c71-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33c71-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33c71-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33c71-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33c71-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

