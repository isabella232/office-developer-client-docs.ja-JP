---
title: プロバイダー テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408972"
---
# <a name="provider-tables"></a><span data-ttu-id="b65d7-103">プロバイダー テーブル</span><span class="sxs-lookup"><span data-stu-id="b65d7-103">Provider Tables</span></span>

  
  
<span data-ttu-id="b65d7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b65d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b65d7-105">プロバイダー テーブルには、サービス プロバイダーに関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b65d7-105">A provider table contains information about service providers.</span></span> <span data-ttu-id="b65d7-106">MAPI によって実装され、クライアントによって使用される 2 つの異なるプロバイダー テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="b65d7-106">There are two different provider tables, both implemented by MAPI and used by clients.</span></span> <span data-ttu-id="b65d7-107">[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出すことによってアクセスされる最初のテーブルには、現在のプロファイルのすべてのプロバイダーに関する情報が保持されます。</span><span class="sxs-lookup"><span data-stu-id="b65d7-107">The first table, accessed by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, holds information about all of the providers for the current profile.</span></span> <span data-ttu-id="b65d7-108">[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)を介してアクセスされる 2 番目のテーブルは、メッセージ サービスのすべてのサービス プロバイダーに関する情報を格納するテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b65d7-108">The second table, accessed through [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), creates a table that stores information about all of the service providers for a message service.</span></span>
  
<span data-ttu-id="b65d7-109">これら 2 つのテーブルには別の違いがあります。</span><span class="sxs-lookup"><span data-stu-id="b65d7-109">These two tables have another difference.</span></span> <span data-ttu-id="b65d7-110">**IMsgServiceAdmin::GetProviderTable** で使用できるプロバイダー テーブルには、サービス プロバイダーを表す行だけが含まれますが **、IProviderAdmin::GetProviderTable** を使用して使用できるテーブルには、サービス プロバイダーに関連付けられた追加情報を表す行が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b65d7-110">The provider table available through **IMsgServiceAdmin::GetProviderTable** contains only rows that represent service providers while the table available through **IProviderAdmin::GetProviderTable** may include rows that represent additional information associated with a service provider.</span></span> <span data-ttu-id="b65d7-111">この追加の情報は、MAPISVC.INF の "Sections" キーワードを使用してプロファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b65d7-111">This extra information is added to the profile with the "Sections" keyword of MAPISVC.INF.</span></span> <span data-ttu-id="b65d7-112">プロバイダーに追加のプロファイル セクションがある場合、これらのセクションの **MAPIUID** 値は PR_SERVICE_EXTRA_UIDS ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md))**プロパティに** 格納されます。</span><span class="sxs-lookup"><span data-stu-id="b65d7-112">When a provider has extra profile sections, it stores the **MAPIUID** values for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="b65d7-113">**PR_SERVICE_EXTRA_UIDS** メッセージ サービス プロファイル セクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="b65d7-113">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="b65d7-114">次のプロパティは、両方の種類のプロバイダー テーブルで必要な列セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="b65d7-114">The following properties make up the required column set in both types of provider tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b65d7-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b65d7-116">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-116">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b65d7-117">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-117">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b65d7-118">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-118">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b65d7-119">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-119">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b65d7-120">**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-120">**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b65d7-121">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-121">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b65d7-122">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-122">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b65d7-123">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-123">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b65d7-124">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b65d7-124">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="b65d7-125">プロバイダー テーブルは、現在のトランスポートの順序を表示したり、変更したりするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b65d7-125">The provider table can be used to display the current transport order or to change it.</span></span> <span data-ttu-id="b65d7-126">現在の順序を表示するには、PR_RESOURCE_TYPE プロパティが設定されている行のみを取得MAPI_TRANSPORT_PROVIDER。</span><span class="sxs-lookup"><span data-stu-id="b65d7-126">To display the current order, build a restriction to retrieve only those rows with the **PR_RESOURCE_TYPE** property set to MAPI_TRANSPORT_PROVIDER.</span></span> <span data-ttu-id="b65d7-127">次に **PR_PROVIDER_ORDINAL** を並べ替えキーとして使用し [、IMAPITable::QueryRows](imapitable-queryrows.md) メソッドまたは [HrQueryAllRows](hrqueryallrows.md) 関数を使用してすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="b65d7-127">Then use **PR_PROVIDER_ORDINAL** as a sort key to sort the table and retrieve all the rows with either the [IMAPITable::QueryRows](imapitable-queryrows.md) method or the [HrQueryAllRows](hrqueryallrows.md) function.</span></span> 
  
<span data-ttu-id="b65d7-128">トランスポートの順序を変更するには、同じ制限を適用して行を取得します。</span><span class="sxs-lookup"><span data-stu-id="b65d7-128">To change the transport order, apply the same restriction and retrieve the rows.</span></span> <span data-ttu-id="b65d7-129">次に、トランスポート プロバイダーの一意の識別子 **PR_PROVIDER_UID** プロパティから値の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="b65d7-129">Then create an array of values from the **PR_PROVIDER_UID** property that represents the unique identifiers for the transport providers.</span></span> <span data-ttu-id="b65d7-130">識別子が目的の順序である場合は、 [それらを IMsgServiceAdmin::MsgServiceTransportOrder メソッドに渡](imsgserviceadmin-msgservicetransportorder.md) します。</span><span class="sxs-lookup"><span data-stu-id="b65d7-130">When the identifiers are in the desired order, pass them to the [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) method.</span></span> 
  
<span data-ttu-id="b65d7-131">プロバイダー テーブルが使用可能にされた後、プロバイダーの追加や削除など、後続の変更は反映されません。</span><span class="sxs-lookup"><span data-stu-id="b65d7-131">After a provider table has been made available, it will not reflect subsequent changes, such as the addition or deletion of a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b65d7-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="b65d7-132">See also</span></span>



[<span data-ttu-id="b65d7-133">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="b65d7-133">MAPI Tables</span></span>](mapi-tables.md)

