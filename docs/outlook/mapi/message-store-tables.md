---
title: メッセージストアテーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405353"
---
# <a name="message-store-tables"></a><span data-ttu-id="2fd5c-103">メッセージストアテーブル</span><span class="sxs-lookup"><span data-stu-id="2fd5c-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="2fd5c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fd5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fd5c-105">メッセージストアテーブルには、現在のプロファイルのメッセージストアプロバイダーに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2fd5c-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="2fd5c-106">mapi によって実装され、クライアントによって使用される、すべての mapi セッションに対してメッセージストアテーブルが1つあります。</span><span class="sxs-lookup"><span data-stu-id="2fd5c-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="2fd5c-107">クライアントは、このテーブルを使用して、特定のプロバイダーのすべてのインスタンスを検索したり、特定のメッセージストアを見つけたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="2fd5c-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="2fd5c-108">メッセージストアテーブルが動的である。</span><span class="sxs-lookup"><span data-stu-id="2fd5c-108">The message store table is dynamic.</span></span> <span data-ttu-id="2fd5c-109">クライアントアプリケーションのユーザーがプロファイルを編集し、既定のメッセージストアを変更した場合は、影響を受けるメッセージストアの**PR_DEFAULT_STORE**プロパティの値がすぐに更新されます。</span><span class="sxs-lookup"><span data-stu-id="2fd5c-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="2fd5c-110">クライアントは、 [imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メソッドを呼び出すことによって、メッセージストアテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2fd5c-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="2fd5c-111">次のプロパティを使用して、メッセージストアテーブルで必要な列セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="2fd5c-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2fd5c-112">**PR_DEFAULT_STORE**([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2fd5c-113">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2fd5c-114">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2fd5c-115">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2fd5c-116">**PR_MDB_PROVIDER**([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2fd5c-117">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2fd5c-118">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2fd5c-119">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2fd5c-120">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2fd5c-121">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2fd5c-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2fd5c-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="2fd5c-122">See also</span></span>



[<span data-ttu-id="2fd5c-123">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="2fd5c-123">MAPI Tables</span></span>](mapi-tables.md)

