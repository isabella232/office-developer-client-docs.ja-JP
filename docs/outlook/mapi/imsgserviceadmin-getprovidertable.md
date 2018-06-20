---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4272edef5b1b72944d1d27f0e4dd99ee4956aa57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800975"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="fd071-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="fd071-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="fd071-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd071-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd071-105">プロバイダー テーブル、プロファイル内のサービス プロバイダーの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fd071-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="fd071-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="fd071-106">Parameters</span></span>

 <span data-ttu-id="fd071-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd071-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fd071-108">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="fd071-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="fd071-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="fd071-109">_lppTable_</span></span>
  
> <span data-ttu-id="fd071-110">[out]プロバイダー テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fd071-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd071-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fd071-111">Return value</span></span>

<span data-ttu-id="fd071-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd071-112">S_OK</span></span> 
  
> <span data-ttu-id="fd071-113">プロバイダー テーブルは正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="fd071-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd071-114">備考</span><span class="sxs-lookup"><span data-stu-id="fd071-114">Remarks</span></span>

<span data-ttu-id="fd071-115">**IMsgServiceAdmin::GetProviderTable**メソッドでは、MAPI プロバイダーのテーブル、すべてのアドレス帳、メッセージ ・ ストア、およびプロファイルに現在インストールされているトランスポート プロバイダーの一覧が表示されるテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fd071-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="fd071-116">[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)メソッドによって返されるプロバイダー テーブルとは異なり、 **IMsgServiceAdmin::GetProviderTable**によって返されるプロバイダー テーブルが関連付けられている情報を表す追加の行を含めることはできません。プロファイルのサービスのプロバイダーの 1 つまたは複数の</span><span class="sxs-lookup"><span data-stu-id="fd071-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="fd071-117">削除されている、または使用中だが、削除対象としてマークされているプロバイダーは、プロバイダーの表には含まれません。</span><span class="sxs-lookup"><span data-stu-id="fd071-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="fd071-118">プロバイダー テーブルへの後の追加や、プロファイルからの削除が表に反映されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="fd071-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="fd071-119">プロバイダー プロファイルがない場合は、 **GetProviderTable**は、0 個の行と S_OK の戻り値を持つテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="fd071-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="fd071-120">プロバイダー テーブル内の列の一覧は、[プロバイダーのテーブル](provider-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd071-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fd071-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="fd071-121">Notes to callers</span></span>

<span data-ttu-id="fd071-122">トランスポートの順番でプロバイダーのテーブルの行を取得するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fd071-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="fd071-123">MAPI_TRANSPORT_PROVIDER と**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) のプロパティに一致するプロパティの制限を適用する[IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd071-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="fd071-124">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) の列でテーブルを並べ替えるには[IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd071-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="fd071-125">テーブルの行を取得する[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd071-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="fd071-126">代わりにこれらの呼び出しは、すべての適切なデータ構造体が渡されると、 [HrQueryAllRows](hrqueryallrows.md)関数を 1 つの呼び出しを行うには。</span><span class="sxs-lookup"><span data-stu-id="fd071-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="fd071-127">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) の列にそれぞれの行を取得する場合は、 [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)への呼び出しのトランスポートの順番を設定するのには、この**MAPIUID**の構造体の配列を使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd071-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="fd071-128">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定は、次を行います。</span><span class="sxs-lookup"><span data-stu-id="fd071-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="fd071-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドによって、プロバイダーのテーブルの最初のアクティブな列に返されるデータの unicode 文字列の種類を設定します。</span><span class="sxs-lookup"><span data-stu-id="fd071-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="fd071-130">プロバイダー テーブルの最初のアクティブな列は、これらの列がテーブルの呼び出しを[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドに含まれているプロバイダーの前に、 **QueryColumns**メソッドを返します。</span><span class="sxs-lookup"><span data-stu-id="fd071-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="fd071-131">**スプーラー**によって、プロバイダーのテーブルの最初のアクティブな行に返されるデータの unicode 文字列の種類を設定します。</span><span class="sxs-lookup"><span data-stu-id="fd071-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="fd071-132">プロバイダーのテーブルの最初のアクティブな行は、これらの行をテーブル呼び出し**SetColumns**を含むプロバイダーをする前に**スプーラー**を返しますです。</span><span class="sxs-lookup"><span data-stu-id="fd071-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="fd071-133">プロバイダー テーブルを含んでいるクライアントは、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出す前に、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類を制御します。</span><span class="sxs-lookup"><span data-stu-id="fd071-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fd071-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd071-134">See also</span></span>



[<span data-ttu-id="fd071-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="fd071-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="fd071-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="fd071-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="fd071-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="fd071-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="fd071-138">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd071-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

