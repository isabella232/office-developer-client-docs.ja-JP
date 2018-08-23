---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e9b9ae316749659c6fc6a043bfb72c49010ccc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800397"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="502f9-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="502f9-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="502f9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="502f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="502f9-105">アドレス帳コンテナー、または送信メッセージの受信者の一覧には、新しい受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="502f9-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a><span data-ttu-id="502f9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="502f9-106">Parameters</span></span>

 <span data-ttu-id="502f9-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="502f9-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="502f9-108">[in]ダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="502f9-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="502f9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="502f9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="502f9-110">[in]使用されるテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="502f9-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="502f9-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="502f9-111">The following flag can be set:</span></span>
    
<span data-ttu-id="502f9-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="502f9-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="502f9-113">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="502f9-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="502f9-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="502f9-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="502f9-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="502f9-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="502f9-116">[in]_LpEIDContainer_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="502f9-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="502f9-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="502f9-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="502f9-118">[in]新しい受信者を追加するコンテナーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="502f9-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="502f9-119">_CbEIDContainer_パラメーターが 0 の場合は、 **NewEntry**メソッドは[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)メソッドが呼び出された場合と同様の受信者のエントリの識別子と、テンプレートの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="502f9-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="502f9-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="502f9-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="502f9-121">[in]_LpEIDNewEntryTpl_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="502f9-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="502f9-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="502f9-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="502f9-123">[in]新しい受信者を作成するために使用する 1 回限りのテンプレートへのポインター。</span><span class="sxs-lookup"><span data-stu-id="502f9-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="502f9-124">0、 _cbEIDNewEntryTpl_し、 _lpEIDNewEntryTpl_が NULL の場合、 **NewEntry**は、ユーザーが新しいエントリを追加するためのテンプレートの一覧から選択できますダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="502f9-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="502f9-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="502f9-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="502f9-126">[out]_LppEIDNewEntry_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="502f9-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="502f9-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="502f9-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="502f9-128">[out]新しい受信者のエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="502f9-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="502f9-129">�߂�l</span><span class="sxs-lookup"><span data-stu-id="502f9-129">Return value</span></span>

<span data-ttu-id="502f9-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="502f9-130">S_OK</span></span> 
  
> <span data-ttu-id="502f9-131">新しいアドレス帳のエントリが正しく作成されました。</span><span class="sxs-lookup"><span data-stu-id="502f9-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="502f9-132">注釈</span><span class="sxs-lookup"><span data-stu-id="502f9-132">Remarks</span></span>

<span data-ttu-id="502f9-133">**NewEntry**メソッドは、新しいアドレス帳のエントリ、または送信するメッセージに対処するために使用するコンテナーに直接追加するを作成します。</span><span class="sxs-lookup"><span data-stu-id="502f9-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="502f9-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="502f9-134">Notes to callers</span></span>

<span data-ttu-id="502f9-135">特定のコンテナーに追加する新しいエントリを設定する場合は、コンテナーのエントリの識別子とエントリの識別子のバイト数を_cbEIDContainer_に_lpEIDContainer_を設定します。</span><span class="sxs-lookup"><span data-stu-id="502f9-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="502f9-136">送信メッセージの受信者の一覧に追加する新しいエントリを設定する場合は、NULL と 0 を_cbEIDContainer_に_lpEIDContainer_を設定します。</span><span class="sxs-lookup"><span data-stu-id="502f9-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="502f9-137">作成するエントリの種類を選択するのにはクライアント アプリケーションのユーザーを許可する場合は、 _cbEIDNewEntryTpl_内の 0 と_lpEIDNewEntryTpl_に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="502f9-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="502f9-138">**NewEntry**メソッドには、MAPI の一時テーブルでサポートされている MAPI アドレス帳プロバイダーによって、セッションのテンプレートの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="502f9-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="502f9-139">各テンプレートには、1 つまたは複数のアドレスの種類の受信者のエントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="502f9-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="502f9-140">新しいエントリのエントリの識別子を保持する場合は、 _lpcbEIDNewEntry_および_lppEIDNewEntry_パラメーターで有効なポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="502f9-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="502f9-141">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって操作を終了したら、このエントリの識別子を解放する責任があります。</span><span class="sxs-lookup"><span data-stu-id="502f9-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="502f9-142">変更可能なコンテナーに新しいエントリを追加するのには特定のテンプレートを使用するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="502f9-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="502f9-143">開くには、移動先のコンテナーでは、 [IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出すし、コンテナーのエントリの識別子を_lpEntryID_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="502f9-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="502f9-144">、移動先のコンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すし、IID_IMAPITable に**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) に_ulPropTag_パラメーターは、 _lpiid_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="502f9-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="502f9-145">コンテナーでは、新しいエントリを作成するため、サポートされるすべてのテンプレートを一覧表示する一時テーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="502f9-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="502f9-146">特定の種類のエントリを作成するためのテンプレートを表す行を取得します。</span><span class="sxs-lookup"><span data-stu-id="502f9-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="502f9-147">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) の列では、テンプレートでサポートされているアドレスの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="502f9-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="502f9-148">**NewEntry**メソッドを呼び出すし、 _lpEIDNewEntryTpl_を選択したテンプレートのエントリの識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="502f9-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="502f9-149">エントリの識別子は、一時テーブル内のテンプレートの行から**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) の列になります。</span><span class="sxs-lookup"><span data-stu-id="502f9-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="502f9-150">_CbEIDContainer_の 0 と_lpEIDContainer_に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="502f9-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="502f9-151">新しいエントリのエントリの識別子を保持する場合は、 _lppEIDNewEntry_パラメーターに有効なポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="502f9-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="502f9-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="502f9-152">See also</span></span>



[<span data-ttu-id="502f9-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="502f9-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="502f9-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="502f9-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="502f9-155">PidTagCreateTemplates 標準プロパティ Property</span><span class="sxs-lookup"><span data-stu-id="502f9-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="502f9-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="502f9-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

