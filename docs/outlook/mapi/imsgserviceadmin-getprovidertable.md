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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428768"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="e42cb-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="e42cb-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="e42cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e42cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e42cb-105">プロファイル内のサービス プロバイダーの一覧であるプロバイダー テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e42cb-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="e42cb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e42cb-106">Parameters</span></span>

 <span data-ttu-id="e42cb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e42cb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e42cb-108">[in]常に NULL。</span><span class="sxs-lookup"><span data-stu-id="e42cb-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="e42cb-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e42cb-109">_lppTable_</span></span>
  
> <span data-ttu-id="e42cb-110">[out]プロバイダー テーブルへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="e42cb-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e42cb-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="e42cb-111">Return value</span></span>

<span data-ttu-id="e42cb-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e42cb-112">S_OK</span></span> 
  
> <span data-ttu-id="e42cb-113">プロバイダー テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="e42cb-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e42cb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e42cb-114">Remarks</span></span>

<span data-ttu-id="e42cb-115">**IMsgServiceAdmin::GetProviderTable** メソッドは、プロファイルに現在インストールされているすべてのアドレス帳、メッセージ ストア、およびトランスポート プロバイダーを一覧表示する MAPI プロバイダー テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e42cb-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="e42cb-116">[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)メソッドを介して返されるプロバイダー テーブルとは異なり **、IMsgServiceAdmin::GetProviderTable** を介して返されるプロバイダー テーブルには、プロファイル内の 1 つ以上のサービス プロバイダーに関連付けられた情報を表す追加の行を含めできません。</span><span class="sxs-lookup"><span data-stu-id="e42cb-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="e42cb-117">削除されたプロバイダー、または使用されているが削除のマークが付いているプロバイダーは、プロバイダー テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="e42cb-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="e42cb-118">プロバイダー テーブルは静的です。つまり、プロファイルへの以降の追加またはプロファイルからの削除はテーブルに反映されません。</span><span class="sxs-lookup"><span data-stu-id="e42cb-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="e42cb-119">プロファイルにプロバイダーがない場合 **、GetProviderTable** は行が 0 のテーブルを返し、その値S_OK返します。</span><span class="sxs-lookup"><span data-stu-id="e42cb-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="e42cb-120">プロバイダー テーブル内の列の完全な一覧については、「Provider [Table」を参照してください](provider-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="e42cb-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e42cb-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e42cb-121">Notes to callers</span></span>

<span data-ttu-id="e42cb-122">プロバイダー テーブルの行をトランスポート順序で取得するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="e42cb-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="e42cb-123">[IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出して、PR_RESOURCE_TYPE **(** [PidTagResourceType](pidtagresourcetype-canonical-property.md)) プロパティと一致するプロパティ制限を適用MAPI_TRANSPORT_PROVIDER。</span><span class="sxs-lookup"><span data-stu-id="e42cb-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="e42cb-124">[IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出して、テーブルを [PR_PROVIDER_ORDINAL **]** 列 [(PidTagProviderOrdinal)](pidtagproviderordinal-canonical-property.md)列で並べ替えてください。</span><span class="sxs-lookup"><span data-stu-id="e42cb-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="e42cb-125">[IMAPITable::QueryRows メソッドを呼](imapitable-queryrows.md)び出して、テーブルの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="e42cb-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="e42cb-126">これらの呼び出しの代わりに、適切なすべてのデータ構造が渡された [HrQueryAllRows](hrqueryallrows.md) 関数を 1 回呼び出す方法があります。</span><span class="sxs-lookup"><span data-stu-id="e42cb-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="e42cb-127">各行で **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を取得する場合は、 **この MAPIUID** 構造体の配列を使用して [、IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)の呼び出しでトランスポート順序を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e42cb-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="e42cb-128">_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると、次の手順が実行されます。</span><span class="sxs-lookup"><span data-stu-id="e42cb-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="e42cb-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドによってプロバイダー テーブルの最初のアクティブな列に対して返されるデータの文字列型を Unicode に設定します。</span><span class="sxs-lookup"><span data-stu-id="e42cb-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="e42cb-130">プロバイダー テーブルの最初のアクティブな列は、テーブルを含むプロバイダーが [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出す前に **QueryColumns** メソッドが返す列です。</span><span class="sxs-lookup"><span data-stu-id="e42cb-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="e42cb-131">QueryRows によってプロバイダー テーブルの最初のアクティブな行に対して返されるデータの文字列型を **Unicode に設定します**。</span><span class="sxs-lookup"><span data-stu-id="e42cb-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="e42cb-132">プロバイダー テーブルの最初のアクティブな行は、テーブルを含むプロバイダーが **SetColumns** を呼び出す前に **QueryRows** が返す行です。</span><span class="sxs-lookup"><span data-stu-id="e42cb-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="e42cb-133">プロバイダー テーブルを含むクライアントが[IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出す前に[、IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類を制御します。</span><span class="sxs-lookup"><span data-stu-id="e42cb-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e42cb-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="e42cb-134">See also</span></span>



[<span data-ttu-id="e42cb-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="e42cb-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="e42cb-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="e42cb-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="e42cb-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="e42cb-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="e42cb-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e42cb-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

