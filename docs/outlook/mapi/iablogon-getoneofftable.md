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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b8a6d74df3749a5445d95ad392f7f88d27190bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800345"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="5386f-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="5386f-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="5386f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5386f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5386f-105">送信メッセージの受信者の一覧に追加する受信者を作成するための 1 回限りのテンプレートのテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="5386f-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5386f-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5386f-106">Parameters</span></span>

 <span data-ttu-id="5386f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5386f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5386f-108">[in]テーブルに含まれている文字列型の列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5386f-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="5386f-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5386f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5386f-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5386f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5386f-111">Unicode 形式では、文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="5386f-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="5386f-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="5386f-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="5386f-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5386f-113">_lppTable_</span></span>
  
> <span data-ttu-id="5386f-114">[out]一時テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5386f-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5386f-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5386f-115">Return value</span></span>

<span data-ttu-id="5386f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5386f-116">S_OK</span></span> 
  
> <span data-ttu-id="5386f-117">一時テーブルが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="5386f-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="5386f-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5386f-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5386f-119">MAPI_UNICODE フラグが設定されたアドレス帳プロバイダーが Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、アドレス帳プロバイダーは、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5386f-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="5386f-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5386f-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5386f-121">アドレス帳プロバイダーは、1 回限りのテンプレートを提供していません。</span><span class="sxs-lookup"><span data-stu-id="5386f-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5386f-122">備考</span><span class="sxs-lookup"><span data-stu-id="5386f-122">Remarks</span></span>

<span data-ttu-id="5386f-123">MAPI では、受信者を作成するのには使用可能な 1 回限りのテンプレートを作成する**GetOneOffTable**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5386f-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="5386f-124">新しい受信者は、送信メッセージの受信者の一覧に追加されます。</span><span class="sxs-lookup"><span data-stu-id="5386f-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="5386f-125">アドレス帳プロバイダーは、MAPI のテンプレートの変更を通知するために一時テーブルの通知をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5386f-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="5386f-126">MAPI では、動的更新を有効にするのには開いている一時テーブルを保持します。</span><span class="sxs-lookup"><span data-stu-id="5386f-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="5386f-127">アドレス帳プロバイダーは、そのコンテナーの一時テーブルをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="5386f-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="5386f-128">呼び出し元は、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すと、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを要求して、この一時テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="5386f-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="5386f-129">このテーブルを使用できるテンプレートを使用すると、コンテナーに受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="5386f-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="5386f-130">一時テーブルの 2 つの種類の違いについては、[一時テーブルを実装する](implementing-one-off-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5386f-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="5386f-131">アドレス帳プロバイダーの一時テーブルに必要な列のリストは、[一時テーブル](one-off-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5386f-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5386f-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="5386f-132">See also</span></span>



[<span data-ttu-id="5386f-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="5386f-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="5386f-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="5386f-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="5386f-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="5386f-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="5386f-136">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5386f-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

