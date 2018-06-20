---
title: プロバイダー テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a613bd744a113b4378c5bef94fb51f6ae3aa4041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803707"
---
# <a name="provider-tables"></a><span data-ttu-id="49a77-103">プロバイダー テーブル</span><span class="sxs-lookup"><span data-stu-id="49a77-103">Provider Tables</span></span>

  
  
<span data-ttu-id="49a77-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49a77-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49a77-105">プロバイダー テーブルには、サービス プロバイダーに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="49a77-105">A provider table contains information about service providers.</span></span> <span data-ttu-id="49a77-106">別のプロバイダーの 2 つのテーブルは、MAPI によって実装され、クライアントによって使用される両方。</span><span class="sxs-lookup"><span data-stu-id="49a77-106">There are two different provider tables, both implemented by MAPI and used by clients.</span></span> <span data-ttu-id="49a77-107">アクセス、 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出すことによって、最初の表は、すべての現在のプロファイル プロバイダーに関する情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="49a77-107">The first table, accessed by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, holds information about all of the providers for the current profile.</span></span> <span data-ttu-id="49a77-108">2 番目のテーブルでは、 [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)を使用してアクセスは、すべてのメッセージ サービスのサービス プロバイダーに関する情報を格納するテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="49a77-108">The second table, accessed through [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), creates a table that stores information about all of the service providers for a message service.</span></span>
  
<span data-ttu-id="49a77-109">これら 2 つのテーブルには、他の違いがあります。</span><span class="sxs-lookup"><span data-stu-id="49a77-109">These two tables have another difference.</span></span> <span data-ttu-id="49a77-110">**IMsgServiceAdmin::GetProviderTable**を通じて利用可能なプロバイダーのテーブルには、サービス ・ プロバイダーを表し、 **IProviderAdmin::GetProviderTable**を使用可能なテーブルを表す行を含めることがある行だけが含まれています。サービス プロバイダーに関連付けられている追加の情報です。</span><span class="sxs-lookup"><span data-stu-id="49a77-110">The provider table available through **IMsgServiceAdmin::GetProviderTable** contains only rows that represent service providers while the table available through **IProviderAdmin::GetProviderTable** may include rows that represent additional information associated with a service provider.</span></span> <span data-ttu-id="49a77-111">MAPISVC.INF の「項目」キーワードを使用してプロファイルには、この余分な情報が追加されます。</span><span class="sxs-lookup"><span data-stu-id="49a77-111">This extra information is added to the profile with the "Sections" keyword of MAPISVC.INF.</span></span> <span data-ttu-id="49a77-112">プロバイダーに追加のプロファイル セクションが設定されているときは、 **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) のプロパティでこれらのセクションで**MAPIUID**の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="49a77-112">When a provider has extra profile sections, it stores the **MAPIUID** values for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="49a77-113">**PR_SERVICE_EXTRA_UIDS**は、サービス プロファイルの [メッセージ] セクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="49a77-113">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="49a77-114">次のプロパティは、必須の列が両方の種類のプロバイダーのテーブルで設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="49a77-114">The following properties make up the required column set in both types of provider tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49a77-115">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="49a77-116">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-116">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="49a77-117">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-117">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="49a77-118">**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-118">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="49a77-119">**PR_PROVIDER_ORDINAL**([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-119">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="49a77-120">**PR_PROVIDER_UID**([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-120">**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="49a77-121">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-121">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="49a77-122">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-122">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="49a77-123">**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-123">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="49a77-124">**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="49a77-124">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="49a77-125">現在のトランスポートの順番を表示する、またはそれを変更するのには、プロバイダーのテーブルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="49a77-125">The provider table can be used to display the current transport order or to change it.</span></span> <span data-ttu-id="49a77-126">現在の注文を表示するには、MAPI_TRANSPORT_PROVIDER に**PR_RESOURCE_TYPE**プロパティを使用してこれらの行だけを取得するために制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="49a77-126">To display the current order, build a restriction to retrieve only those rows with the **PR_RESOURCE_TYPE** property set to MAPI_TRANSPORT_PROVIDER.</span></span> <span data-ttu-id="49a77-127">使用して**PR_PROVIDER_ORDINAL**の並べ替えキーとしてテーブルを並べ替えるし、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドまたは[HrQueryAllRows](hrqueryallrows.md)関数のいずれかでのすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="49a77-127">Then use **PR_PROVIDER_ORDINAL** as a sort key to sort the table and retrieve all the rows with either the [IMAPITable::QueryRows](imapitable-queryrows.md) method or the [HrQueryAllRows](hrqueryallrows.md) function.</span></span> 
  
<span data-ttu-id="49a77-128">トランスポートの順番を変更するに同じ制限を適用し、行を取得します。</span><span class="sxs-lookup"><span data-stu-id="49a77-128">To change the transport order, apply the same restriction and retrieve the rows.</span></span> <span data-ttu-id="49a77-129">トランスポート プロバイダーの一意の識別子を表す、 **PR_PROVIDER_UID**プロパティからの値の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="49a77-129">Then create an array of values from the **PR_PROVIDER_UID** property that represents the unique identifiers for the transport providers.</span></span> <span data-ttu-id="49a77-130">識別子は、目的の順序では、ときに、 [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="49a77-130">When the identifiers are in the desired order, pass them to the [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) method.</span></span> 
  
<span data-ttu-id="49a77-131">使用可能なプロバイダーのテーブルが行われて、追加またはプロバイダーの削除など、その後の変更は反映されません。</span><span class="sxs-lookup"><span data-stu-id="49a77-131">After a provider table has been made available, it will not reflect subsequent changes, such as the addition or deletion of a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49a77-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="49a77-132">See also</span></span>



[<span data-ttu-id="49a77-133">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="49a77-133">MAPI Tables</span></span>](mapi-tables.md)

