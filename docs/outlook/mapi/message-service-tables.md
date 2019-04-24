---
title: メッセージサービステーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356911"
---
# <a name="message-service-tables"></a><span data-ttu-id="ec54a-103">メッセージサービステーブル</span><span class="sxs-lookup"><span data-stu-id="ec54a-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="ec54a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec54a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec54a-105">メッセージサービステーブルには、現在のプロファイルのメッセージサービスに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec54a-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="ec54a-106">mapi によって実装され、構成のサポートを提供する特殊な目的のクライアントアプリケーションによって使用される、すべての mapi セッションに対して1つのメッセージサービステーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="ec54a-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="ec54a-107">メッセージサービステーブルは静的テーブルです。</span><span class="sxs-lookup"><span data-stu-id="ec54a-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="ec54a-108">クライアントは、 [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)メソッドを呼び出して、メッセージサービステーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ec54a-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="ec54a-109">次のプロパティは、メッセージサービステーブルで必要な列セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="ec54a-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec54a-110">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ec54a-111">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ec54a-112">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ec54a-113">**PR_SERVICE_DLL_NAME**([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ec54a-114">**PR_SERVICE_ENTRY_NAME**([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ec54a-115">**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ec54a-116">**PR_SERVICE_SUPPORT_FILES**([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ec54a-117">**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ec54a-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="ec54a-118">**PR_DISPLAY_NAME**は、メッセージサービスの表示名と既定の並べ替えキー列です。</span><span class="sxs-lookup"><span data-stu-id="ec54a-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="ec54a-119">**PR_INSTANCE_KEY**は、行を一意に識別する、テーブルのインデックス列として機能します。</span><span class="sxs-lookup"><span data-stu-id="ec54a-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="ec54a-120">**PR_RESOURCE_FLAGS**メッセージサービスの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec54a-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="ec54a-121">**PR_SERVICE_DLL_NAME**は、メッセージサービスの実装を含む DLL の名前です。</span><span class="sxs-lookup"><span data-stu-id="ec54a-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="ec54a-122">**PR_SERVICE_ENTRY_NAME**は、 [msgserviceentry](msgserviceentry.md)プロトタイプに準拠したメッセージサービスのエントリポイント関数の名前です。</span><span class="sxs-lookup"><span data-stu-id="ec54a-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="ec54a-123">**PR_SERVICE_NAME**は、mapisvc.inf の **[Services]** セクションで必須のエントリです。</span><span class="sxs-lookup"><span data-stu-id="ec54a-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="ec54a-124">このプロパティの値は、変更またはローカライズされません。</span><span class="sxs-lookup"><span data-stu-id="ec54a-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="ec54a-125">**PR_SERVICE_NAME**を使用して、メッセージサービスをプログラムで識別できます。</span><span class="sxs-lookup"><span data-stu-id="ec54a-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="ec54a-126">**PR_SERVICE_SUPPORT_FILES**は、メッセージサービスと共にインストールする必要があるファイルの一覧です。</span><span class="sxs-lookup"><span data-stu-id="ec54a-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="ec54a-127">**PR_SERVICE_UID**は、メッセージサービスの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="ec54a-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec54a-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec54a-128">See also</span></span>



[<span data-ttu-id="ec54a-129">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="ec54a-129">MAPI Tables</span></span>](mapi-tables.md)

