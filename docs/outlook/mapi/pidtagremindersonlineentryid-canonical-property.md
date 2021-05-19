---
title: PidTagRemindersOnlineEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d845a37f9248a30dadd4db7722d8bed0f9f8d264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355063"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a><span data-ttu-id="275d2-103">PidTagRemindersOnlineEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="275d2-103">PidTagRemindersOnlineEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="275d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="275d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="275d2-105">アラーム フォルダー **の EntryID** を格納します。</span><span class="sxs-lookup"><span data-stu-id="275d2-105">Contains the **EntryID** of the reminders folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="275d2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="275d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="275d2-107">PR_REM_ONLINE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="275d2-107">PR_REM_ONLINE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="275d2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="275d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="275d2-109">0x36D5</span><span class="sxs-lookup"><span data-stu-id="275d2-109">0x36D5</span></span>  <br/> |
|<span data-ttu-id="275d2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="275d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="275d2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="275d2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="275d2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="275d2-112">Area:</span></span>  <br/> |<span data-ttu-id="275d2-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="275d2-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="275d2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="275d2-114">Remarks</span></span>

<span data-ttu-id="275d2-115">このプロパティは、受信トレイ フォルダーとメッセージ ストアのルート フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="275d2-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="275d2-116">特定のメッセージ ストアのプロパティにアクセスするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="275d2-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="275d2-117">最初に、受信トレイ フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="275d2-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="275d2-118">受信トレイ フォルダーの **EntryID** への参照を取得するには [、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="275d2-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="275d2-119">**IMsgStore::GetReceiveFolder** が成功した場合は、受信トレイと [IMsgStore::OpenEntry](imsgstore-openentry.md)の **EntryID** への参照を使用して受信トレイを開き **、IMAPIFolder** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="275d2-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="275d2-120">**IMsgStore::OpenEntry** が成功した場合は **、IMAPIFolder** オブジェクトと [IMAPIProp::GetProps](imapiprop-getprops.md)への返される参照を使用して、目的のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="275d2-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="275d2-121">手順 1、2、または 3 に失敗した場合は、ルート フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="275d2-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="275d2-122">これを行うには **、IMsgStore::OpenEntry** を使用して **、lpEntryID** に NULL を指定して、メッセージ ストアのルート フォルダーを開き **、IMAPIFolder** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="275d2-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="275d2-123">ルート フォルダーを開くが成功した場合は **、IMAPIFolder** オブジェクトと **IMAPIProp::GetProps** への返される参照を使用して、目的のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="275d2-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="275d2-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="275d2-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="275d2-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="275d2-125">Protocol specifications</span></span>

<span data-ttu-id="275d2-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="275d2-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="275d2-127">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="275d2-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="275d2-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="275d2-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="275d2-129">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="275d2-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="275d2-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="275d2-130">Header files</span></span>

<span data-ttu-id="275d2-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="275d2-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="275d2-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="275d2-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="275d2-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="275d2-133">Mapitags.h</span></span>
  
> <span data-ttu-id="275d2-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="275d2-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="275d2-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="275d2-135">See also</span></span>



[<span data-ttu-id="275d2-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="275d2-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="275d2-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="275d2-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="275d2-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="275d2-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="275d2-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="275d2-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

