---
title: プロバイダーテーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328463"
---
# <a name="provider-tables"></a><span data-ttu-id="d2110-103">プロバイダーテーブル</span><span class="sxs-lookup"><span data-stu-id="d2110-103">Provider Tables</span></span>

  
  
<span data-ttu-id="d2110-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2110-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2110-105">プロバイダーテーブルには、サービスプロバイダーに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d2110-105">A provider table contains information about service providers.</span></span> <span data-ttu-id="d2110-106">2つの異なるプロバイダーテーブルがあり、両方とも MAPI によって実装され、クライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="d2110-106">There are two different provider tables, both implemented by MAPI and used by clients.</span></span> <span data-ttu-id="d2110-107">[IMsgServiceAdmin:: getprovidertable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出してアクセスする最初のテーブルは、現在のプロファイルのすべてのプロバイダーに関する情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="d2110-107">The first table, accessed by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, holds information about all of the providers for the current profile.</span></span> <span data-ttu-id="d2110-108">[IProviderAdmin:: getprovidertable](iprovideradmin-getprovidertable.md)を通じてアクセスされる2番目の表は、メッセージサービスのすべてのサービスプロバイダーに関する情報を格納するテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="d2110-108">The second table, accessed through [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), creates a table that stores information about all of the service providers for a message service.</span></span>
  
<span data-ttu-id="d2110-109">これらの2つのテーブルには別の違いがあります。</span><span class="sxs-lookup"><span data-stu-id="d2110-109">These two tables have another difference.</span></span> <span data-ttu-id="d2110-110">**IMsgServiceAdmin:: getprovidertable**で利用できるプロバイダテーブルには、サービスプロバイダを表す行のみが含まれていますが、 **IProviderAdmin:: getprovidertable**を通じて使用可能な表には、を表す行を含めることができます。サービスプロバイダーに関連付けられている追加情報。</span><span class="sxs-lookup"><span data-stu-id="d2110-110">The provider table available through **IMsgServiceAdmin::GetProviderTable** contains only rows that represent service providers while the table available through **IProviderAdmin::GetProviderTable** may include rows that represent additional information associated with a service provider.</span></span> <span data-ttu-id="d2110-111">この追加情報は、mapisvc.inf の "Sections" キーワードを使用してプロファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d2110-111">This extra information is added to the profile with the "Sections" keyword of MAPISVC.INF.</span></span> <span data-ttu-id="d2110-112">プロバイダーに特別なプロファイルセクションがある場合は、これらのセクションの**MAPIUID**値を**PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) プロパティに格納します。</span><span class="sxs-lookup"><span data-stu-id="d2110-112">When a provider has extra profile sections, it stores the **MAPIUID** values for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="d2110-113">**PR_SERVICE_EXTRA_UIDS**は、[メッセージサービスプロファイル] セクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="d2110-113">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="d2110-114">次のプロパティは、両方の種類のプロバイダーテーブルで必要な列セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="d2110-114">The following properties make up the required column set in both types of provider tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2110-115">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d2110-116">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-116">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d2110-117">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-117">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d2110-118">**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-118">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d2110-119">**PR_PROVIDER_ORDINAL**([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-119">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d2110-120">**PR_PROVIDER_UID**([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-120">**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d2110-121">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-121">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d2110-122">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-122">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d2110-123">**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-123">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d2110-124">**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d2110-124">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="d2110-125">プロバイダーテーブルを使用して、現在のトランスポート順序を表示したり、変更したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="d2110-125">The provider table can be used to display the current transport order or to change it.</span></span> <span data-ttu-id="d2110-126">現在の順序を表示するには、 **PR_RESOURCE_TYPE**プロパティが MAPI_TRANSPORT_PROVIDER に設定されている行のみを取得する制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="d2110-126">To display the current order, build a restriction to retrieve only those rows with the **PR_RESOURCE_TYPE** property set to MAPI_TRANSPORT_PROVIDER.</span></span> <span data-ttu-id="d2110-127">その後、 **PR_PROVIDER_ORDINAL**を並べ替えキーとして使用して、テーブルを並べ替え、 [IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドまたは[hrqueryallrows](hrqueryallrows.md)関数のいずれかを使用してすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d2110-127">Then use **PR_PROVIDER_ORDINAL** as a sort key to sort the table and retrieve all the rows with either the [IMAPITable::QueryRows](imapitable-queryrows.md) method or the [HrQueryAllRows](hrqueryallrows.md) function.</span></span> 
  
<span data-ttu-id="d2110-128">トランスポート順序を変更するには、同じ制限を適用して行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d2110-128">To change the transport order, apply the same restriction and retrieve the rows.</span></span> <span data-ttu-id="d2110-129">次に、トランスポートプロバイダーの一意の識別子を表す**PR_PROVIDER_UID**プロパティから値の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="d2110-129">Then create an array of values from the **PR_PROVIDER_UID** property that represents the unique identifiers for the transport providers.</span></span> <span data-ttu-id="d2110-130">識別子が目的の順序になったら、 [IMsgServiceAdmin:: msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md)メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="d2110-130">When the identifiers are in the desired order, pass them to the [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) method.</span></span> 
  
<span data-ttu-id="d2110-131">プロバイダーテーブルが使用可能になると、その後の変更 (プロバイダーの追加や削除など) は反映されません。</span><span class="sxs-lookup"><span data-stu-id="d2110-131">After a provider table has been made available, it will not reflect subsequent changes, such as the addition or deletion of a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2110-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2110-132">See also</span></span>



[<span data-ttu-id="d2110-133">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="d2110-133">MAPI Tables</span></span>](mapi-tables.md)

