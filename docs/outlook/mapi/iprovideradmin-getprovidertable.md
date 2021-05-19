---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434474"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="fcf1d-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="fcf1d-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="fcf1d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcf1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcf1d-105">メッセージ サービスのプロバイダー テーブル 、メッセージ サービス内のサービス プロバイダーの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="fcf1d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fcf1d-106">Parameters</span></span>

 <span data-ttu-id="fcf1d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fcf1d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fcf1d-108">[in]プロバイダー テーブルの列で返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="fcf1d-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="fcf1d-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fcf1d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fcf1d-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="fcf1d-112">このフラグMAPI_UNICODE設定されていない場合、列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="fcf1d-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="fcf1d-113">_lppTable_</span></span>
  
> <span data-ttu-id="fcf1d-114">[out]プロバイダー テーブルへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fcf1d-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="fcf1d-115">Return value</span></span>

<span data-ttu-id="fcf1d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcf1d-116">S_OK</span></span> 
  
> <span data-ttu-id="fcf1d-117">プロバイダー テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcf1d-118">注釈</span><span class="sxs-lookup"><span data-stu-id="fcf1d-118">Remarks</span></span>

<span data-ttu-id="fcf1d-119">**IProviderAdmin::GetProviderTable** メソッドは、メッセージ サービス内の各サービス プロバイダーに関する情報を含む MAPI が保持するテーブルであるメッセージ サービスのプロバイダー テーブルへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="fcf1d-120">[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドによって返されるプロバイダー テーブルとは異なり **、IProviderAdmin::GetProviderTable** によって返されるプロバイダー テーブルには、メッセージ サービス内の 1 つ以上のサービス プロバイダーに関連付けられている情報を表す追加の行が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="fcf1d-121">この追加の情報は、Mapisvc.inf ファイルの "Sections" キーワードを使用してプロファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="fcf1d-122">プロバイダーに追加のプロファイル セクションがある場合、これらのセクションの **MAPIUID** 構造は PR_SERVICE_EXTRA_UIDS ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md))**プロパティに** 格納されます。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="fcf1d-123">**PR_SERVICE_EXTRA_UIDS** メッセージ サービス プロファイル セクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="fcf1d-124">削除されたプロバイダー、または使用されているが削除のマークが付いているプロバイダーは、プロバイダー テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="fcf1d-125">プロバイダー テーブルは静的です。つまり、メッセージ サービスに対する後続の追加または削除はテーブルに反映されません。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="fcf1d-126">メッセージ サービスにプロバイダーがない場合 **、IProviderAdmin::GetProviderTable** は、行が 0 のテーブルを返し、S_OK値を返します。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="fcf1d-127">_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="fcf1d-128">このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="fcf1d-129">プロバイダー テーブル内の列の完全な一覧については、「Provider [Table」を参照してください](provider-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fcf1d-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="fcf1d-130">Notes to callers</span></span>

<span data-ttu-id="fcf1d-131">プロバイダー テーブルの行をトランスポートの順序で取得するには、テーブルを [プロパティ] **列** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) 列PR_PROVIDER_ORDINAL並べ替えてください。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="fcf1d-132">サービス プロバイダーを表す行 (余分な行を含めずに) のみを取得するには、PR_RESOURCE_TYPE **(** [PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列の PT_ERROR の値を持つ行に取得を制限します。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fcf1d-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="fcf1d-133">MFCMAPI reference</span></span>

<span data-ttu-id="fcf1d-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fcf1d-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="fcf1d-135">**File**</span></span>|<span data-ttu-id="fcf1d-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="fcf1d-136">**Function**</span></span>|<span data-ttu-id="fcf1d-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="fcf1d-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fcf1d-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="fcf1d-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="fcf1d-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="fcf1d-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="fcf1d-140">MFCMAPI は **、IProviderAdmin::GetProviderTable** メソッドを使用して、新しいダイアログ ボックスでレンダリングするプロバイダーのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="fcf1d-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcf1d-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcf1d-141">See also</span></span>



[<span data-ttu-id="fcf1d-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="fcf1d-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="fcf1d-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="fcf1d-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="fcf1d-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="fcf1d-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="fcf1d-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="fcf1d-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="fcf1d-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="fcf1d-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="fcf1d-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fcf1d-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


<span data-ttu-id="fcf1d-148">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="fcf1d-148">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

