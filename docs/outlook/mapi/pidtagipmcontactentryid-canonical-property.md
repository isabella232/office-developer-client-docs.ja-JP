---
title: PidTagIpmContactEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c09d4848373a530e80298d6c01ad3d411d9eb60e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567413"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a><span data-ttu-id="39935-103">PidTagIpmContactEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="39935-103">PidTagIpmContactEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="39935-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39935-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39935-105">Outlook の連絡先フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="39935-105">Contains the **EntryID** of the Outlook Contacts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39935-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="39935-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39935-107">PR_IPM_CONTACT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="39935-107">PR_IPM_CONTACT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="39935-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="39935-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39935-109">0x36D1</span><span class="sxs-lookup"><span data-stu-id="39935-109">0x36D1</span></span>  <br/> |
|<span data-ttu-id="39935-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="39935-110">Data type:</span></span>  <br/> |<span data-ttu-id="39935-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="39935-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="39935-112">領域:</span><span class="sxs-lookup"><span data-stu-id="39935-112">Area:</span></span>  <br/> |<span data-ttu-id="39935-113">Folder</span><span class="sxs-lookup"><span data-stu-id="39935-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39935-114">注釈</span><span class="sxs-lookup"><span data-stu-id="39935-114">Remarks</span></span>

<span data-ttu-id="39935-115">このプロパティは、[受信トレイ] フォルダーで、メッセージ ・ ストアのルート フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="39935-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="39935-116">特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="39935-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="39935-117">最初に、受信トレイ フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="39935-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="39935-118">**IMsgStore::GetReceiveFolder**を使用すると、受信トレイ フォルダーの**エントリ Id**への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="39935-118">Use **IMsgStore::GetReceiveFolder** to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="39935-119">**IMsgStore::GetReceiveFolder**が成功した場合は、受信トレイを開き、 **IMAPIFolder**オブジェクトへの参照を取得する、受信トレイと**IMsgStore::OpenEntry**の**エントリ Id**への参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="39935-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and **IMsgStore::OpenEntry** to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="39935-120">**IMsgStore::OpenEntry**が成功した場合は、目的のプロパティを取得する**IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="39935-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="39935-121">1、2、または 3 の手順が失敗した場合は、ルート フォルダーのプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="39935-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="39935-122">**IMsgStore::OpenEntry**の場合は NULL を指定することを使用するには、* * lpEntryID * * には、メッセージ ・ ストアのルート フォルダーを開き、 **IMAPIFolder**オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="39935-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for ** lpEntryID **, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="39935-123">ルート フォルダーを開くときに成功した場合は、目的のプロパティを取得するのには、 **IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="39935-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="39935-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="39935-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39935-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="39935-125">Protocol specifications</span></span>

<span data-ttu-id="39935-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39935-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39935-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="39935-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39935-128">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39935-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39935-129">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="39935-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="39935-130">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39935-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39935-131">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="39935-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39935-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="39935-132">Header files</span></span>

<span data-ttu-id="39935-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39935-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="39935-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="39935-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="39935-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="39935-135">Mapitags.h</span></span>
  
> <span data-ttu-id="39935-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="39935-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39935-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="39935-137">See also</span></span>



[<span data-ttu-id="39935-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="39935-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39935-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="39935-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39935-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="39935-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39935-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="39935-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

