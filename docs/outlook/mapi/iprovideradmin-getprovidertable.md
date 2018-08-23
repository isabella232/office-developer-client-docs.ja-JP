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
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801167"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="428c3-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="428c3-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="428c3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="428c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="428c3-105">メッセージ サービスのプロバイダーのテーブル、メッセージ サービスのサービス プロバイダーの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="428c3-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="428c3-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="428c3-106">Parameters</span></span>

 <span data-ttu-id="428c3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="428c3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="428c3-108">[in]プロバイダー テーブルの列で返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="428c3-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="428c3-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="428c3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="428c3-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="428c3-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="428c3-111">Unicode 形式では、文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="428c3-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="428c3-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の列です。</span><span class="sxs-lookup"><span data-stu-id="428c3-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="428c3-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="428c3-113">_lppTable_</span></span>
  
> <span data-ttu-id="428c3-114">[out]プロバイダー テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="428c3-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="428c3-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="428c3-115">Return value</span></span>

<span data-ttu-id="428c3-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="428c3-116">S_OK</span></span> 
  
> <span data-ttu-id="428c3-117">プロバイダー テーブルは正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="428c3-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="428c3-118">注釈</span><span class="sxs-lookup"><span data-stu-id="428c3-118">Remarks</span></span>

<span data-ttu-id="428c3-119">**IProviderAdmin::GetProviderTable**メソッドは、メッセージ サービスのプロバイダーのテーブル、MAPI は、メッセージ サービスでは、各サービス プロバイダーに関する情報が含まれていることを保持するテーブルへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="428c3-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="428c3-120">、 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドによって返されるプロバイダーのテーブルとは異なり、 **IProviderAdmin::GetProviderTable**によって返されるプロバイダーのテーブルがのいずれかに関連付けられている情報を表す追加の行を含めることがメッセージ サービスのサービス プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="428c3-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="428c3-121">この追加情報は、Mapisvc.inf ファイルの「項目」キーワードを使用してプロファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="428c3-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="428c3-122">プロバイダーに追加のプロファイル セクションが設定されているときは、 **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) のプロパティでこれらのセクションの**MAPIUID**構造体を格納します。</span><span class="sxs-lookup"><span data-stu-id="428c3-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="428c3-123">**PR_SERVICE_EXTRA_UIDS**は、サービス プロファイルの [メッセージ] セクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="428c3-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="428c3-124">削除されている、または使用中だが、削除対象としてマークされているプロバイダーは、プロバイダーの表には含まれません。</span><span class="sxs-lookup"><span data-stu-id="428c3-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="428c3-125">プロバイダー テーブルにそれ以降に追加された機能またはメッセージ サービスからの削除が表に反映されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="428c3-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="428c3-126">メッセージ サービスには、プロバイダーがなければ、 **IProviderAdmin::GetProviderTable**は、0 個の行と S_OK の戻り値を持つテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="428c3-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="428c3-127">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="428c3-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="428c3-128">このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="428c3-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="428c3-129">プロバイダー テーブル内の列の一覧は、[プロバイダーのテーブル](provider-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="428c3-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="428c3-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="428c3-130">Notes to callers</span></span>

<span data-ttu-id="428c3-131">トランスポートの順番でプロバイダーのテーブルの行を取得するには、 **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) の列でテーブルをソートします。</span><span class="sxs-lookup"><span data-stu-id="428c3-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="428c3-132">(せず、余分な行を含む) のサービス ・ プロバイダーを表す行のみを取得するには、PT_ERROR の**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))] 列の値を持つ行が取得されるを制限します。</span><span class="sxs-lookup"><span data-stu-id="428c3-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="428c3-133">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="428c3-133">MFCMAPI reference</span></span>

<span data-ttu-id="428c3-134">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="428c3-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="428c3-135">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="428c3-135">**File**</span></span>|<span data-ttu-id="428c3-136">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="428c3-136">**Function**</span></span>|<span data-ttu-id="428c3-137">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="428c3-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="428c3-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="428c3-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="428c3-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="428c3-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="428c3-140">MFCMAPI では、 **IProviderAdmin::GetProviderTable**メソッドを使用して、新しいダイアログ ボックスに表示するプロバイダーのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="428c3-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="428c3-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="428c3-141">See also</span></span>



[<span data-ttu-id="428c3-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="428c3-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="428c3-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="428c3-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="428c3-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="428c3-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="428c3-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="428c3-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="428c3-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="428c3-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="428c3-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="428c3-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


<span data-ttu-id="428c3-148">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="428c3-148">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

