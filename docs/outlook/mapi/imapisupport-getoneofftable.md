---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 51cd838164e3de28ab33d6ab8a08a021360f3183
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800737"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="21d30-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="21d30-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="21d30-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21d30-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21d30-105">MAPI の一時テーブル (すべてのアドレスが新しい受信者を作成するためのサポートについてプロバイダーを登録しているテンプレートの一覧) へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="21d30-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="21d30-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="21d30-106">Parameters</span></span>

 <span data-ttu-id="21d30-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="21d30-107">_ulFlags_</span></span>
  
> <span data-ttu-id="21d30-108">[in]文字列型の列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="21d30-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="21d30-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="21d30-109">The following flag can be set:</span></span>
    
<span data-ttu-id="21d30-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="21d30-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="21d30-111">Unicode 形式では、文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="21d30-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="21d30-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="21d30-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="21d30-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="21d30-113">_lppTable_</span></span>
  
> <span data-ttu-id="21d30-114">[out]一時テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="21d30-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="21d30-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="21d30-115">Return value</span></span>

<span data-ttu-id="21d30-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="21d30-116">S_OK</span></span> 
  
> <span data-ttu-id="21d30-117">一時テーブルが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="21d30-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21d30-118">備考</span><span class="sxs-lookup"><span data-stu-id="21d30-118">Remarks</span></span>

<span data-ttu-id="21d30-119">アドレス帳プロバイダーのサポート オブジェクトの**IMAPISupport::GetOneOffTable**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="21d30-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="21d30-120">アドレス帳プロバイダーは、新しい受信者を作成するためのテンプレートの完全な一覧を取得するために**GetOneOffTable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21d30-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="21d30-121">このテーブルには、MAPI をサポートしているテンプレートと同様に、セッションでアクティブになっているアドレス帳プロバイダーがサポートするテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="21d30-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="21d30-122">新しく作成された受信者は、メッセージの宛先を使用することができますか、アドレス帳コンテナーに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="21d30-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="21d30-123">必須の列を一時テーブルの設定を構成するプロパティのリストは、[一時テーブル](one-off-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21d30-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="21d30-124">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="21d30-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="21d30-125">このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="21d30-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="21d30-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="21d30-126">Notes to callers</span></span>

<span data-ttu-id="21d30-127">この一時テーブルへの変更の通知を受信する登録している場合は、他のプロバイダーの一時テーブルへの変更の通知も表示されます。</span><span class="sxs-lookup"><span data-stu-id="21d30-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="21d30-128">これらの通知に基づき、現在のセッション中に追加される新しいアドレスの種類をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="21d30-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21d30-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="21d30-129">See also</span></span>



[<span data-ttu-id="21d30-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="21d30-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="21d30-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="21d30-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="21d30-132">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="21d30-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="21d30-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="21d30-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="21d30-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="21d30-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="21d30-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="21d30-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="21d30-136">PidTagCreateTemplates の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="21d30-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="21d30-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="21d30-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="21d30-138">一時テーブル</span><span class="sxs-lookup"><span data-stu-id="21d30-138">One-Off Tables</span></span>](one-off-tables.md)

