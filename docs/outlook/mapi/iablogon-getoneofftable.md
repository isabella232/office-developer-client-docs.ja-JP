---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411877"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="f534f-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="f534f-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="f534f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f534f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f534f-105">送信メッセージの受信者リストに追加する受信者を作成するための、1回限りのテンプレートのテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="f534f-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f534f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f534f-106">Parameters</span></span>

 <span data-ttu-id="f534f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f534f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f534f-108">順番テーブルに含まれる文字列型 (string) の列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f534f-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="f534f-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f534f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f534f-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f534f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f534f-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="f534f-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="f534f-112">MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="f534f-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="f534f-113">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="f534f-113">_lppTable_</span></span>
  
> <span data-ttu-id="f534f-114">読み上げ1回限りのテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f534f-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f534f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="f534f-115">Return value</span></span>

<span data-ttu-id="f534f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f534f-116">S_OK</span></span> 
  
> <span data-ttu-id="f534f-117">1回限りのテーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="f534f-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="f534f-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f534f-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f534f-119">MAPI_UNICODE フラグが設定されていて、アドレス帳プロバイダーが unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、アドレス帳プロバイダーが unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f534f-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="f534f-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f534f-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f534f-121">アドレス帳プロバイダーでは、1回限りのテンプレートは提供されません。</span><span class="sxs-lookup"><span data-stu-id="f534f-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f534f-122">注釈</span><span class="sxs-lookup"><span data-stu-id="f534f-122">Remarks</span></span>

<span data-ttu-id="f534f-123">MAPI は、 **getoneofftable**メソッドを呼び出して、受信者を作成するために1回限りのテンプレートを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f534f-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="f534f-124">新しい受信者が送信メッセージの受信者一覧に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f534f-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="f534f-125">アドレス帳プロバイダーは、テンプレートの変更を MAPI に通知するために、1回限りのテーブルに対する通知をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f534f-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="f534f-126">MAPI は、動的更新を有効にするために、1回限りのテーブルを開いたままにします。</span><span class="sxs-lookup"><span data-stu-id="f534f-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="f534f-127">また、アドレス帳プロバイダーは、各コンテナーに対して1回限りのテーブルをサポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f534f-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="f534f-128">発信者は、コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求することによって、この1回限りのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="f534f-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="f534f-129">この表で使用できるテンプレートは、受信者をコンテナーに追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f534f-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="f534f-130">2種類の一度限りのテーブルの違いについては、「 [1 回限りのテーブルの実装](implementing-one-off-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f534f-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="f534f-131">アドレス帳プロバイダーの1回限りのテーブルで必要な列の一覧については、「 [1 回限りのテーブル](one-off-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f534f-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f534f-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="f534f-132">See also</span></span>



[<span data-ttu-id="f534f-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="f534f-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="f534f-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="f534f-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="f534f-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="f534f-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="f534f-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f534f-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

