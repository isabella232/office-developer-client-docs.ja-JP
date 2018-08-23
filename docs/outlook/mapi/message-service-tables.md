---
title: メッセージ サービス テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 569c1bd7ee2f4ac6c321f234be2954a57715549b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576671"
---
# <a name="message-service-tables"></a><span data-ttu-id="7e472-103">メッセージ サービス テーブル</span><span class="sxs-lookup"><span data-stu-id="7e472-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="7e472-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e472-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e472-105">メッセージ サービス テーブルには、現在のプロファイル内のメッセージ サービスに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7e472-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="7e472-106">MAPI セッションごとに MAPI によって実装され、構成のサポートを提供する特別な目的のクライアント アプリケーションによって使用されるメッセージ サービスの 1 つのテーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="7e472-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="7e472-107">メッセージ サービス テーブルは、静的なテーブルです。</span><span class="sxs-lookup"><span data-stu-id="7e472-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="7e472-108">クライアントは、 [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)メソッドを呼び出して、メッセージ サービス テーブルをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7e472-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="7e472-109">次のプロパティは、メッセージ サービス テーブルを設定する必要な列を構成します。</span><span class="sxs-lookup"><span data-stu-id="7e472-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e472-110">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e472-111">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="7e472-112">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e472-113">**PR_SERVICE_DLL_NAME**([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="7e472-114">**PR_SERVICE_ENTRY_NAME**([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e472-115">**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="7e472-116">**PR_SERVICE_SUPPORT_FILES**([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7e472-117">**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e472-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="7e472-118">**PR_DISPLAY_NAME**は、メッセージ サービス、および既定の並べ替えのキー列の表示可能な名前です。</span><span class="sxs-lookup"><span data-stu-id="7e472-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="7e472-119">**PR_INSTANCE_KEY**は、行を一意に識別するテーブルのインデックス列として機能します。</span><span class="sxs-lookup"><span data-stu-id="7e472-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="7e472-120">**PR_RESOURCE_FLAGS**では、メッセージ サービスの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e472-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="7e472-121">**PR_SERVICE_DLL_NAME**は、メッセージ サービスの実装を含む DLL の名前です。</span><span class="sxs-lookup"><span data-stu-id="7e472-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="7e472-122">**PR_SERVICE_ENTRY_NAME**は、 [MSGSERVICEENTRY](msgserviceentry.md)のプロトタイプに準拠しているメッセージ サービスのエントリ ポイント関数の名前です。</span><span class="sxs-lookup"><span data-stu-id="7e472-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="7e472-123">**PR_SERVICE_NAME**は、MAPISVC.INF の **[サービス]** セクションで必要なエントリです。</span><span class="sxs-lookup"><span data-stu-id="7e472-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="7e472-124">このプロパティの値の変更またはローカライズされたことはありませんが。</span><span class="sxs-lookup"><span data-stu-id="7e472-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="7e472-125">メッセージ サービスをプログラムで識別する**PR_SERVICE_NAME**を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7e472-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="7e472-126">**PR_SERVICE_SUPPORT_FILES**は、メッセージ サービスをインストールする必要があるファイルの一覧です。</span><span class="sxs-lookup"><span data-stu-id="7e472-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="7e472-127">**PR_SERVICE_UID**は、メッセージ サービスの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="7e472-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e472-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e472-128">See also</span></span>



[<span data-ttu-id="7e472-129">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="7e472-129">MAPI Tables</span></span>](mapi-tables.md)

