---
title: メッセージ ストア テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801649"
---
# <a name="message-store-tables"></a><span data-ttu-id="55c49-103">メッセージ ストア テーブル</span><span class="sxs-lookup"><span data-stu-id="55c49-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="55c49-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55c49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55c49-105">メッセージ ストアのテーブルには、現在のプロファイルで、メッセージ ストア プロバイダーに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="55c49-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="55c49-106">MAPI セッションごとに MAPI によって実装され、クライアントによって使用されるメッセージ ストアの 1 つのテーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="55c49-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="55c49-107">クライアントは、特定のプロバイダーのすべてのインスタンスを検索する、または特定のメッセージ ストアを検索するのには次の表を使用できます。</span><span class="sxs-lookup"><span data-stu-id="55c49-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="55c49-108">メッセージ ストアのテーブルは、動的です。</span><span class="sxs-lookup"><span data-stu-id="55c49-108">The message store table is dynamic.</span></span> <span data-ttu-id="55c49-109">クライアント アプリケーションのユーザーは、プロファイルを編集する場合は、 **PR_DEFAULT_STORE**の値など、既定のメッセージ ストアを変更する影響を受けるメッセージ ストアのプロパティをすぐに更新されます。</span><span class="sxs-lookup"><span data-stu-id="55c49-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="55c49-110">クライアントは、 [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)メソッドを呼び出して、メッセージ ストアのテーブルをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="55c49-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="55c49-111">次のプロパティは、メッセージ ストアのテーブルの設定の必要な列を構成します。</span><span class="sxs-lookup"><span data-stu-id="55c49-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55c49-112">**PR_DEFAULT_STORE**([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="55c49-113">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="55c49-114">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="55c49-115">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="55c49-116">**PR_MDB_PROVIDER**([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="55c49-117">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="55c49-118">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="55c49-119">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="55c49-120">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="55c49-121">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="55c49-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55c49-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="55c49-122">See also</span></span>



[<span data-ttu-id="55c49-123">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="55c49-123">MAPI Tables</span></span>](mapi-tables.md)

