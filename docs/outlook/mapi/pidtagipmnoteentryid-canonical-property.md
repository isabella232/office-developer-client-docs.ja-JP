---
title: PidTagIpmNoteEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3fdaa7edef50224ff2687201c5b19f61d31f49e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580951"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a><span data-ttu-id="58579-103">PidTagIpmNoteEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58579-103">PidTagIpmNoteEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="58579-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58579-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58579-105">Outlook のメモ フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="58579-105">Contains the **EntryID** of the Outlook Notes folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58579-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="58579-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58579-107">PR_IPM_NOTE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="58579-107">PR_IPM_NOTE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="58579-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="58579-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58579-109">0x36D3</span><span class="sxs-lookup"><span data-stu-id="58579-109">0x36D3</span></span>  <br/> |
|<span data-ttu-id="58579-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="58579-110">Data type:</span></span>  <br/> |<span data-ttu-id="58579-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="58579-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="58579-112">領域:</span><span class="sxs-lookup"><span data-stu-id="58579-112">Area:</span></span>  <br/> |<span data-ttu-id="58579-113">Folder</span><span class="sxs-lookup"><span data-stu-id="58579-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58579-114">注釈</span><span class="sxs-lookup"><span data-stu-id="58579-114">Remarks</span></span>

<span data-ttu-id="58579-115">このプロパティは、メッセージ ・ ストアのルート フォルダーと同様に、[受信トレイ] フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="58579-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="58579-116">特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="58579-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="58579-117">最初に、受信トレイ フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="58579-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="58579-118">[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用すると、受信トレイ フォルダーの**エントリ Id**への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="58579-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="58579-119">場合 * * IMsgStore::GetReceiveFolder * * 成功するは、受信トレイと[IMsgStore::OpenEntry](imsgstore-openentry.md)の**エントリ Id**への参照を使用して、受信トレイを開き、 **IMAPIFolder**オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="58579-119">If ** IMsgStore::GetReceiveFolder ** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="58579-120">**IMsgStore::OpenEntry**が成功した場合は、目的のプロパティを取得する**IMAPIFolder**オブジェクトと[IMAPIProp::GetProps](imapiprop-getprops.md)に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="58579-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="58579-121">1、2、または 3 の手順が失敗した場合は、ルート フォルダーのプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="58579-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="58579-122">そのためには、 **IMsgStore::OpenEntry**、 **lpEntryID**のメッセージ ・ ストアのルート フォルダーを開き、 **IMAPIFolder**オブジェクトへの参照を取得するのには NULL を指定するを使用します。</span><span class="sxs-lookup"><span data-stu-id="58579-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="58579-123">ルート フォルダーを開くときに成功した場合は、目的のプロパティを取得するのには、 **IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="58579-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="58579-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="58579-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58579-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="58579-125">Protocol specifications</span></span>

<span data-ttu-id="58579-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58579-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58579-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="58579-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58579-128">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58579-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58579-129">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="58579-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="58579-130">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58579-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58579-131">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="58579-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58579-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="58579-132">Header files</span></span>

<span data-ttu-id="58579-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58579-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="58579-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="58579-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="58579-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="58579-135">Mapitags.h</span></span>
  
> <span data-ttu-id="58579-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="58579-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58579-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="58579-137">See also</span></span>



[<span data-ttu-id="58579-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="58579-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58579-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="58579-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58579-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="58579-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58579-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="58579-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

