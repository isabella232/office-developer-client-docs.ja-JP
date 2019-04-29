---
title: imapisupportgetoneofftable
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412759"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="90bcd-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="90bcd-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="90bcd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90bcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90bcd-105">MAPI の1回限りのテーブルへのポインター (すべてのアドレス帳プロバイダーが新しい受信者を作成するためにサポートするテンプレートのリスト) を返します。</span><span class="sxs-lookup"><span data-stu-id="90bcd-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="90bcd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90bcd-106">Parameters</span></span>

 <span data-ttu-id="90bcd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90bcd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="90bcd-108">順番文字列列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="90bcd-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="90bcd-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="90bcd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="90bcd-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="90bcd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="90bcd-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="90bcd-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="90bcd-112">MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="90bcd-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="90bcd-113">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="90bcd-113">_lppTable_</span></span>
  
> <span data-ttu-id="90bcd-114">読み上げ1回限りのテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="90bcd-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90bcd-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="90bcd-115">Return value</span></span>

<span data-ttu-id="90bcd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="90bcd-116">S_OK</span></span> 
  
> <span data-ttu-id="90bcd-117">1回限りのテーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="90bcd-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90bcd-118">注釈</span><span class="sxs-lookup"><span data-stu-id="90bcd-118">Remarks</span></span>

<span data-ttu-id="90bcd-119">**imapisupport:: getoneofftable**メソッドは、アドレス帳プロバイダーサポートオブジェクトに対して実装されています。</span><span class="sxs-lookup"><span data-stu-id="90bcd-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="90bcd-120">アドレス帳プロバイダーは、 **getoneofftable**を呼び出して、新しい受信者を作成するためのテンプレートの完全なリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="90bcd-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="90bcd-121">この表には、セッションのサポートでアクティブになっているブックプロバイダーと MAPI がサポートするテンプレートのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="90bcd-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="90bcd-122">新しく作成された受信者を使用して、メッセージの宛先を指定することも、アドレス帳コンテナーに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="90bcd-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="90bcd-123">1回限りのテーブルで必要な列セットを構成するプロパティの一覧については、「 [1 回限りのテーブル](one-off-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90bcd-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="90bcd-124">_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="90bcd-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="90bcd-125">このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="90bcd-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="90bcd-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="90bcd-126">Notes to callers</span></span>

<span data-ttu-id="90bcd-127">この1回限りのテーブルへの変更の通知を受信するように登録されている場合は、他のプロバイダーの1回限りのテーブルへの変更について通知を受け取ることもあります。</span><span class="sxs-lookup"><span data-stu-id="90bcd-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="90bcd-128">これらの通知に基づいて、現在のセッション中に追加された新しいアドレスの種類をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="90bcd-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90bcd-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="90bcd-129">See also</span></span>



[<span data-ttu-id="90bcd-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="90bcd-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="90bcd-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="90bcd-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="90bcd-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90bcd-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="90bcd-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="90bcd-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="90bcd-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="90bcd-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="90bcd-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="90bcd-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="90bcd-136">PidTagCreateTemplates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90bcd-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="90bcd-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="90bcd-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="90bcd-138">1回限りのテーブル</span><span class="sxs-lookup"><span data-stu-id="90bcd-138">One-Off Tables</span></span>](one-off-tables.md)

