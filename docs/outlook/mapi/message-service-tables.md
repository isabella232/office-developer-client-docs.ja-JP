---
title: メッセージ サービス テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422496"
---
# <a name="message-service-tables"></a><span data-ttu-id="8e51b-103">メッセージ サービス テーブル</span><span class="sxs-lookup"><span data-stu-id="8e51b-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="8e51b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e51b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e51b-105">メッセージ サービス テーブルには、現在のプロファイルのメッセージ サービスに関する情報が含まれている。</span><span class="sxs-lookup"><span data-stu-id="8e51b-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="8e51b-106">MAPI によって実装され、構成サポートを提供する特別な目的のクライアント アプリケーションによって使用される、MAPI セッションごとに 1 つのメッセージ サービス テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="8e51b-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="8e51b-107">メッセージ サービス テーブルは静的テーブルです。</span><span class="sxs-lookup"><span data-stu-id="8e51b-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="8e51b-108">クライアントは [、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) メソッドを呼び出して、メッセージ サービス テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8e51b-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="8e51b-109">次のプロパティは、メッセージ サービス テーブルで必要な列セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="8e51b-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e51b-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8e51b-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="8e51b-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8e51b-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="8e51b-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8e51b-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="8e51b-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8e51b-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e51b-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="8e51b-118">**PR_DISPLAY_NAME** は、メッセージ サービスの表示可能な名前と既定の並べ替えキー列です。</span><span class="sxs-lookup"><span data-stu-id="8e51b-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="8e51b-119">**PR_INSTANCE_KEY** テーブルのインデックス列として機能し、行を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="8e51b-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="8e51b-120">**PR_RESOURCE_FLAGS** サービスの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8e51b-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="8e51b-121">**PR_SERVICE_DLL_NAME** は、メッセージ サービスの実装を含む DLL の名前です。</span><span class="sxs-lookup"><span data-stu-id="8e51b-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="8e51b-122">**PR_SERVICE_ENTRY_NAME** は [、MSGSERVICEENTRY](msgserviceentry.md) プロトタイプに準拠するメッセージ サービスのエントリ ポイント関数の名前です。</span><span class="sxs-lookup"><span data-stu-id="8e51b-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="8e51b-123">**PR_SERVICE_NAME** MAPISVC.INF の **[サービス] セクションの** 必須エントリです。</span><span class="sxs-lookup"><span data-stu-id="8e51b-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="8e51b-124">このプロパティの値は、変更またはローカライズされません。</span><span class="sxs-lookup"><span data-stu-id="8e51b-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="8e51b-125">**PR_SERVICE_NAME** メッセージ サービスをプログラムで識別するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e51b-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="8e51b-126">**PR_SERVICE_SUPPORT_FILES** は、メッセージ サービスと一緒にインストールする必要があるファイルの一覧です。</span><span class="sxs-lookup"><span data-stu-id="8e51b-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="8e51b-127">**PR_SERVICE_UID** は、メッセージ サービスの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="8e51b-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e51b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e51b-128">See also</span></span>



[<span data-ttu-id="8e51b-129">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="8e51b-129">MAPI Tables</span></span>](mapi-tables.md)

