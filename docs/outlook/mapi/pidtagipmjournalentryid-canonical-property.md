---
title: PidTagIpmJournalEntryId 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b5dfc378a2558e906bec018608e2d2c776090c06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327910"
---
# <a name="pidtagipmjournalentryid-canonical-property"></a><span data-ttu-id="602cb-103">PidTagIpmJournalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="602cb-103">PidTagIpmJournalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="602cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="602cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="602cb-105">Outlook Journal フォルダーの**EntryID**が保存されています。</span><span class="sxs-lookup"><span data-stu-id="602cb-105">Contains the **EntryID** of the Outlook Journal folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="602cb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="602cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="602cb-107">PR_IPM_JOURNAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="602cb-107">PR_IPM_JOURNAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="602cb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="602cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="602cb-109">0x36D2</span><span class="sxs-lookup"><span data-stu-id="602cb-109">0x36D2</span></span>  <br/> |
|<span data-ttu-id="602cb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="602cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="602cb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="602cb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="602cb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="602cb-112">Area:</span></span>  <br/> |<span data-ttu-id="602cb-113">フォルダー</span><span class="sxs-lookup"><span data-stu-id="602cb-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="602cb-114">解説</span><span class="sxs-lookup"><span data-stu-id="602cb-114">Remarks</span></span>

<span data-ttu-id="602cb-115">このプロパティは、受信トレイフォルダー、およびメッセージストアのルートフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="602cb-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="602cb-116">特定のメッセージストアのプロパティにアクセスするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="602cb-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="602cb-117">最初に、[受信トレイ] フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="602cb-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="602cb-118">[IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を使用して、受信トレイフォルダーの**EntryID**への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="602cb-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="602cb-119">**IMsgStore:: getreceivefolder**が成功した場合は、inbox および[IMsgStore:: openentry](imsgstore-openentry.md)の**EntryID**への参照を使用して、受信トレイを開き、 **imapifolder**オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="602cb-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="602cb-120">**IMsgStore:: openentry**に成功した場合は、返された参照を**imapifolder**オブジェクトと[imapifolder:: GetProps](imapiprop-getprops.md)を使用して、目的のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="602cb-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="602cb-121">手順1、2、または3が失敗した場合は、ルートフォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="602cb-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="602cb-122">これを行うには、 **IMsgStore:: openentry**を使用して**l tryid**に NULL を指定し、メッセージストアのルートフォルダーを開き、 **imapifolder**オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="602cb-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="602cb-123">ルートフォルダーを正常に開くことができた場合は、返された参照を**imapifolder**オブジェクトと**imapifolder:: GetProps**を使用して取得し、目的のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="602cb-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="602cb-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="602cb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="602cb-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="602cb-125">Protocol specifications</span></span>

<span data-ttu-id="602cb-126">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="602cb-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="602cb-127">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="602cb-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="602cb-128">[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="602cb-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="602cb-129">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="602cb-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="602cb-130">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="602cb-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="602cb-131">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="602cb-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="602cb-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="602cb-132">Header files</span></span>

<span data-ttu-id="602cb-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="602cb-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="602cb-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="602cb-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="602cb-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="602cb-135">Mapitags.h</span></span>
  
> <span data-ttu-id="602cb-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="602cb-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="602cb-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="602cb-137">See also</span></span>



[<span data-ttu-id="602cb-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="602cb-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="602cb-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="602cb-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="602cb-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="602cb-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="602cb-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="602cb-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

