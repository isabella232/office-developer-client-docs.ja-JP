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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279529"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="88ae4-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="88ae4-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="88ae4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88ae4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88ae4-105">メッセージサービスのプロバイダーテーブルへのアクセスを提供します。これには、メッセージサービスのサービスプロバイダーの一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="88ae4-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="88ae4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="88ae4-106">Parameters</span></span>

 <span data-ttu-id="88ae4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="88ae4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="88ae4-108">順番プロバイダーテーブルの列に返される文字列の型を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="88ae4-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="88ae4-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="88ae4-109">The following flag can be set:</span></span>
    
<span data-ttu-id="88ae4-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="88ae4-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="88ae4-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="88ae4-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="88ae4-112">MAPI_UNICODE フラグが設定されていない場合、列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="88ae4-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="88ae4-113">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="88ae4-113">_lppTable_</span></span>
  
> <span data-ttu-id="88ae4-114">読み上げプロバイダテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="88ae4-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="88ae4-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="88ae4-115">Return value</span></span>

<span data-ttu-id="88ae4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="88ae4-116">S_OK</span></span> 
  
> <span data-ttu-id="88ae4-117">プロバイダーテーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="88ae4-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88ae4-118">解説</span><span class="sxs-lookup"><span data-stu-id="88ae4-118">Remarks</span></span>

<span data-ttu-id="88ae4-119">**IProviderAdmin:: getprovidertable**メソッドは、メッセージサービスのプロバイダーテーブルへのポインターを取得します。これには、メッセージサービスの各サービスプロバイダーに関する情報を含む MAPI が保持するテーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="88ae4-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="88ae4-120">[IMsgServiceAdmin:: getprovidertable](imsgserviceadmin-getprovidertable.md)メソッドによって返されるプロバイダーテーブルとは異なり、 **IProviderAdmin:: getprovidertable**によって返されるプロバイダテーブルには、1つまたは複数のに関連付けられている情報を表す追加の行が含まれている場合があります。メッセージサービスのサービスプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="88ae4-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="88ae4-121">この追加情報は、mapisvc.inf ファイルの "Sections" キーワードを使用して、プロファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="88ae4-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="88ae4-122">プロバイダーに特別なプロファイルセクションがある場合は、これらのセクションの**MAPIUID**構造体を**PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) プロパティに格納します。</span><span class="sxs-lookup"><span data-stu-id="88ae4-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="88ae4-123">**PR_SERVICE_EXTRA_UIDS**は、[メッセージサービスプロファイル] セクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="88ae4-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="88ae4-124">削除されているか、または使用されていて、削除対象としてマークされているプロバイダーは、プロバイダテーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="88ae4-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="88ae4-125">プロバイダーテーブルは静的であるため、メッセージサービスに対する以降の追加または削除は、テーブルには反映されません。</span><span class="sxs-lookup"><span data-stu-id="88ae4-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="88ae4-126">メッセージサービスにプロバイダーがない場合、 **IProviderAdmin:: getprovidertable**は、行が0で、S_OK の戻り値を持つテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="88ae4-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="88ae4-127">_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="88ae4-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="88ae4-128">このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="88ae4-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="88ae4-129">プロバイダテーブルの列の完全なリストについては、「[プロバイダ table](provider-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88ae4-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="88ae4-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="88ae4-130">Notes to callers</span></span>

<span data-ttu-id="88ae4-131">プロバイダーテーブルの行をトランスポート順で取得するには、テーブルを**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) 列で並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="88ae4-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="88ae4-132">その他の行を含めずに、サービスプロバイダーを表す行のみを取得するには、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列に PT_ERROR 値を持つ行に取得することを制限します。</span><span class="sxs-lookup"><span data-stu-id="88ae4-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="88ae4-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="88ae4-133">MFCMAPI reference</span></span>

<span data-ttu-id="88ae4-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88ae4-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="88ae4-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="88ae4-135">**File**</span></span>|<span data-ttu-id="88ae4-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="88ae4-136">**Function**</span></span>|<span data-ttu-id="88ae4-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="88ae4-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="88ae4-138">MsgServiceTableDlg</span><span class="sxs-lookup"><span data-stu-id="88ae4-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="88ae4-139">CMsgServiceTableDlg:: ondisplayitem</span><span class="sxs-lookup"><span data-stu-id="88ae4-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="88ae4-140">mfcmapi は、 **IProviderAdmin:: getprovidertable**メソッドを使用して、新しいダイアログボックスにレンダリングするプロバイダーのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="88ae4-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88ae4-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="88ae4-141">See also</span></span>



[<span data-ttu-id="88ae4-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="88ae4-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="88ae4-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="88ae4-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="88ae4-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="88ae4-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="88ae4-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="88ae4-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="88ae4-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="88ae4-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="88ae4-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="88ae4-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


<span data-ttu-id="88ae4-148">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="88ae4-148">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

