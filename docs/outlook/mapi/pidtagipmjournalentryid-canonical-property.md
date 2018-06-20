---
title: PidTagIpmJournalEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmJournalEntryId
api_type:
- HeaderDef
ms.assetid: a3765b9d-a108-46d7-a97c-a825ae3980be
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e48b3af79656279e3c554cd5093385d894525e43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802901"
---
# <a name="pidtagipmjournalentryid-canonical-property"></a><span data-ttu-id="5fe3a-103">PidTagIpmJournalEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5fe3a-103">PidTagIpmJournalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5fe3a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fe3a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fe3a-105">Outlook の履歴フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-105">Contains the **EntryID** of the Outlook Journal folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fe3a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5fe3a-107">PR_IPM_JOURNAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5fe3a-107">PR_IPM_JOURNAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5fe3a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5fe3a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5fe3a-109">0x36D2</span><span class="sxs-lookup"><span data-stu-id="5fe3a-109">0x36D2</span></span>  <br/> |
|<span data-ttu-id="5fe3a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-110">Data type:</span></span>  <br/> |<span data-ttu-id="5fe3a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fe3a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5fe3a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5fe3a-112">Area:</span></span>  <br/> |<span data-ttu-id="5fe3a-113">Folder</span><span class="sxs-lookup"><span data-stu-id="5fe3a-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fe3a-114">備考</span><span class="sxs-lookup"><span data-stu-id="5fe3a-114">Remarks</span></span>

<span data-ttu-id="5fe3a-115">このプロパティは、メッセージ ・ ストアのルート フォルダーと同様に、[受信トレイ] フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="5fe3a-116">特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="5fe3a-117">最初に、受信トレイ フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="5fe3a-118">[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用すると、受信トレイ フォルダーの**エントリ Id**への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="5fe3a-119">**IMsgStore::GetReceiveFolder**が成功した場合は、受信トレイを開き、 **IMAPIFolder**オブジェクトへの参照を取得する、受信トレイと[IMsgStore::OpenEntry](imsgstore-openentry.md)の**エントリ Id**への参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="5fe3a-120">**IMsgStore::OpenEntry**が成功した場合は、目的のプロパティを取得する**IMAPIFolder**オブジェクトと[IMAPIProp::GetProps](imapiprop-getprops.md)に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="5fe3a-121">1、2、または 3 の手順が失敗した場合は、ルート フォルダーのプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="5fe3a-122">そのためには、 **IMsgStore::OpenEntry**、 **lpEntryID**のメッセージ ・ ストアのルート フォルダーを開き、 **IMAPIFolder**オブジェクトへの参照を取得するのには NULL を指定するを使用します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="5fe3a-123">ルート フォルダーを開くときに成功した場合は、目的のプロパティを取得するのには、 **IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="5fe3a-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5fe3a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5fe3a-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5fe3a-125">Protocol specifications</span></span>

<span data-ttu-id="5fe3a-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe3a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe3a-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5fe3a-128">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe3a-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe3a-129">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="5fe3a-130">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe3a-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe3a-131">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5fe3a-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5fe3a-132">Header files</span></span>

<span data-ttu-id="5fe3a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5fe3a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5fe3a-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="5fe3a-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5fe3a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="5fe3a-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fe3a-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fe3a-137">See also</span></span>



[<span data-ttu-id="5fe3a-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5fe3a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5fe3a-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5fe3a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5fe3a-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5fe3a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5fe3a-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5fe3a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

