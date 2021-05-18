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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f0c79fa098b8bca0518921a25d88a229e23e955
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327903"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a><span data-ttu-id="c8896-103">PidTagIpmContactEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8896-103">PidTagIpmContactEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c8896-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8896-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8896-105">連絡先フォルダー **の EntryID** をOutlookします。</span><span class="sxs-lookup"><span data-stu-id="c8896-105">Contains the **EntryID** of the Outlook Contacts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8896-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c8896-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8896-107">PR_IPM_CONTACT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c8896-107">PR_IPM_CONTACT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c8896-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c8896-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8896-109">0x36D1</span><span class="sxs-lookup"><span data-stu-id="c8896-109">0x36D1</span></span>  <br/> |
|<span data-ttu-id="c8896-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c8896-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8896-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c8896-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c8896-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c8896-112">Area:</span></span>  <br/> |<span data-ttu-id="c8896-113">Folder</span><span class="sxs-lookup"><span data-stu-id="c8896-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8896-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c8896-114">Remarks</span></span>

<span data-ttu-id="c8896-115">このプロパティは、受信トレイ フォルダーとメッセージ ストアのルート フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="c8896-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="c8896-116">特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c8896-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="c8896-117">最初に、受信トレイ フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="c8896-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="c8896-118">受信トレイ フォルダーの **EntryID** への参照を取得するには **、IMsgStore::GetReceiveFolder** を使用します。</span><span class="sxs-lookup"><span data-stu-id="c8896-118">Use **IMsgStore::GetReceiveFolder** to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="c8896-119">**IMsgStore::GetReceiveFolder** が成功した場合は、受信トレイと **IMsgStore::OpenEntry** の **EntryID** への参照を使用して受信トレイを開き **、IMAPIFolder** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="c8896-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and **IMsgStore::OpenEntry** to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="c8896-120">**IMsgStore::OpenEntry** が成功した場合は **、IMAPIFolder** オブジェクトと **IMAPIProp::GetProps** への返される参照を使用して、目的のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="c8896-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="c8896-121">手順 1、2、または 3 に失敗した場合は、ルート フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="c8896-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="c8896-122">これを行うには **、IMsgStore::OpenEntry** を使用し、\*\* lpEntryID \*\*に NULL を指定して、メッセージ ストアのルート フォルダーを開き **、IMAPIFolder** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="c8896-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for \*\* lpEntryID \*\*, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="c8896-123">ルート フォルダーを開くが成功した場合は **、IMAPIFolder** オブジェクトと **IMAPIProp::GetProps** への返される参照を使用して、目的のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="c8896-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="c8896-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c8896-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8896-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c8896-125">Protocol specifications</span></span>

<span data-ttu-id="c8896-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8896-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8896-127">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c8896-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8896-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8896-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8896-129">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8896-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="c8896-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8896-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8896-131">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="c8896-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8896-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c8896-132">Header files</span></span>

<span data-ttu-id="c8896-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8896-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8896-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c8896-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8896-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8896-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c8896-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c8896-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8896-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8896-137">See also</span></span>



[<span data-ttu-id="c8896-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c8896-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8896-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8896-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8896-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8896-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8896-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8896-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

