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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317382"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="8a628-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="8a628-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="8a628-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a628-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a628-105">プロバイダーテーブルへのアクセスを提供します。これは、プロファイル内のサービスプロバイダーの一覧です。</span><span class="sxs-lookup"><span data-stu-id="8a628-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="8a628-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8a628-106">Parameters</span></span>

 <span data-ttu-id="8a628-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a628-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8a628-108">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="8a628-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="8a628-109">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="8a628-109">_lppTable_</span></span>
  
> <span data-ttu-id="8a628-110">読み上げプロバイダテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8a628-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a628-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="8a628-111">Return value</span></span>

<span data-ttu-id="8a628-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a628-112">S_OK</span></span> 
  
> <span data-ttu-id="8a628-113">プロバイダーテーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="8a628-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a628-114">解説</span><span class="sxs-lookup"><span data-stu-id="8a628-114">Remarks</span></span>

<span data-ttu-id="8a628-115">**IMsgServiceAdmin:: getprovidertable**メソッドは、プロファイルに現在インストールされているすべてのアドレス帳、メッセージストア、およびトランスポートプロバイダーを一覧表示した MAPI プロバイダーテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8a628-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="8a628-116">[IProviderAdmin:: getprovidertable](iprovideradmin-getprovidertable.md)メソッドによって返されるプロバイダテーブルとは異なり、 **IMsgServiceAdmin:: getprovidertable**を通じて返されるプロバイダテーブルには、関連付けられている情報を表す追加の行を含めることができませんプロファイルに1つ以上のサービスプロバイダーがある。</span><span class="sxs-lookup"><span data-stu-id="8a628-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="8a628-117">削除されているか、または使用されていて、削除対象としてマークされているプロバイダーは、プロバイダテーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="8a628-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="8a628-118">プロバイダーテーブルは静的であるため、プロファイルからの以降の追加または削除がテーブルに反映されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8a628-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="8a628-119">プロファイルにプロバイダーが含まれていない場合、 **getprovidertable**は0行と S_OK 戻り値を持つテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="8a628-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="8a628-120">プロバイダテーブルの列の完全なリストについては、「[プロバイダ table](provider-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a628-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8a628-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8a628-121">Notes to callers</span></span>

<span data-ttu-id="8a628-122">プロバイダーテーブルの行をトランスポート順で取得するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a628-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="8a628-123">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) プロパティに一致するプロパティ制限を MAPI_TRANSPORT_PROVIDER に適用するには、 [IMAPITable:: Restrict](imapitable-restrict.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8a628-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="8a628-124">**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) 列でテーブルを並べ替えるには、 [IMAPITable:: sorttable](imapitable-sorttable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8a628-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="8a628-125">[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出して、テーブルの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="8a628-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="8a628-126">これらの呼び出しに代わる方法として、すべての適切なデータ構造を渡すことで、 [hrqueryallrows](hrqueryallrows.md)関数への1回の呼び出しを行う方法があります。</span><span class="sxs-lookup"><span data-stu-id="8a628-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="8a628-127">各行の**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を取得する場合は、この**MAPIUID**構造体の配列を使用して、 [IMsgServiceAdmin:: msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md)の呼び出しでトランスポートの順序を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8a628-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="8a628-128">_ulflags_パラメーターに MAPI_UNICODE フラグを設定すると、次の処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="8a628-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="8a628-129">文字列の種類を Unicode に設定し、 [IMAPITable:: querycolumns](imapitable-querycolumns.md)メソッドによってプロバイダテーブルの最初のアクティブな列に対して返されるデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="8a628-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="8a628-130">プロバイダーテーブルの最初のアクティブな列は、テーブルを含むプロバイダーが[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出す前に**querycolumns**メソッドが返す列です。</span><span class="sxs-lookup"><span data-stu-id="8a628-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="8a628-131">**QueryRows**によってプロバイダテーブルの最初のアクティブな行に対して返されるデータについて、文字列の種類を Unicode に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a628-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="8a628-132">プロバイダーテーブルの最初のアクティブな行は、そのテーブルを含むプロバイダーが**SetColumns**を呼び出す前に**QueryRows**が返す行です。</span><span class="sxs-lookup"><span data-stu-id="8a628-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="8a628-133">は、プロバイダーテーブルを含むクライアントが[imapitable:: sorttable](imapitable-sorttable.md)メソッドを呼び出す前に、 [imapitable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類を制御します。</span><span class="sxs-lookup"><span data-stu-id="8a628-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8a628-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a628-134">See also</span></span>



[<span data-ttu-id="8a628-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="8a628-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="8a628-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="8a628-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="8a628-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="8a628-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="8a628-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a628-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

