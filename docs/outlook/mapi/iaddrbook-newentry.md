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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405101"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="f82a2-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="f82a2-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="f82a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f82a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f82a2-105">アドレス帳コンテナーまたは送信メッセージの受信者リストに新しい受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f82a2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f82a2-106">Parameters</span></span>

 <span data-ttu-id="f82a2-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f82a2-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f82a2-108">[in]ダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="f82a2-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="f82a2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f82a2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f82a2-110">[in]使用するテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f82a2-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="f82a2-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f82a2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f82a2-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f82a2-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f82a2-113">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="f82a2-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f82a2-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="f82a2-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f82a2-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="f82a2-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="f82a2-116">[in]  _lpEIDContainer_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="f82a2-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="f82a2-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="f82a2-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="f82a2-118">[in]新しい受信者を追加するコンテナーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f82a2-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="f82a2-119">_cbEIDContainer_ パラメーターが 0 の場合 **、NewEntry** メソッドは [、IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)メソッドが呼び出された場合と同様に、受信者エントリ識別子とテンプレートのリストを返します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="f82a2-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="f82a2-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="f82a2-121">[in]  _lpEIDNewEntryTpl_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="f82a2-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="f82a2-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="f82a2-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="f82a2-123">[in]新しい受信者の作成に使用される 1 回きりテンプレートへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f82a2-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="f82a2-124">_cbEIDNewEntryTpl_ がゼロで _lpEIDNewEntryTpl_ が NULL の場合 **、NewEntry** はダイアログ ボックスを表示し、新しいエントリを追加するテンプレートの一覧からユーザーが選択できます。</span><span class="sxs-lookup"><span data-stu-id="f82a2-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="f82a2-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="f82a2-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="f82a2-126">[out]  _lppEIDNewEntry_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f82a2-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="f82a2-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="f82a2-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="f82a2-128">[out]新しい受信者のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f82a2-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f82a2-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="f82a2-129">Return value</span></span>

<span data-ttu-id="f82a2-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="f82a2-130">S_OK</span></span> 
  
> <span data-ttu-id="f82a2-131">新しいアドレス帳エントリが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="f82a2-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f82a2-132">注釈</span><span class="sxs-lookup"><span data-stu-id="f82a2-132">Remarks</span></span>

<span data-ttu-id="f82a2-133">**NewEntry メソッドは**、新しいアドレス帳エントリを作成し、コンテナーに直接追加するか、送信メッセージのアドレス指定に使用します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f82a2-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f82a2-134">Notes to callers</span></span>

<span data-ttu-id="f82a2-135">新しいエントリを特定のコンテナーに追加する場合は  _、lpEIDContainer_ をコンテナーのエントリ識別子に設定し  _、cbEIDContainer_ をエントリ識別子のバイト 数に設定します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="f82a2-136">送信メッセージの受信者リストに新しいエントリを追加する場合は  _、lpEIDContainer_ を NULL に  _、cbEIDContainer_ を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="f82a2-137">クライアント アプリケーションのユーザーが作成するエントリの種類を選択する場合は _、cbEIDNewEntryTpl で 0、lpEIDNewEntryTpl_ で NULL を渡します。 </span><span class="sxs-lookup"><span data-stu-id="f82a2-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="f82a2-138">**NewEntry メソッドは**、MAPI 一時テーブル、MAPI でサポートされているテンプレートの一覧、およびセッション内の各アドレス帳プロバイダーによって表示されます。</span><span class="sxs-lookup"><span data-stu-id="f82a2-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="f82a2-139">各テンプレートは、1 つ以上のアドレスの種類の受信者エントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f82a2-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="f82a2-140">新しいエントリのエントリ識別子を保持する場合は  _、lpcbEIDNewEntry_ パラメーターと  _lppEIDNewEntry_ パラメーターに有効なポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="f82a2-141">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して終了したら、このエントリ識別子を解放する責任があります。</span><span class="sxs-lookup"><span data-stu-id="f82a2-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="f82a2-142">特定のテンプレートを使用して変更可能なコンテナーに新しいエントリを追加するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="f82a2-143">[IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出して移動先コンテナーを開き _、lpEntryID_ パラメーターをコンテナーのエントリ識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="f82a2-144">宛先コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し _、ulPropTag_ パラメーターを PR_CREATE_TEMPLATES ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) に _、lpiid_ パラメーターを **IID_IMAPITable** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="f82a2-145">コンテナーは、新しいエントリの作成にサポートしているすべてのテンプレートを一覧表示する 1 回のテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="f82a2-146">作成する特定の種類のエントリのテンプレートを表す行を取得します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="f82a2-147">**[PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列は、テンプレートでサポートされているアドレスの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="f82a2-148">**NewEntry メソッドを呼** び出し _、lpEIDNewEntryTpl_ を選択したテンプレートのエントリ識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="f82a2-149">エントリ識別子は、1 回 **PR_ENTRYID** テーブルのテンプレートの行の列 ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列になります。</span><span class="sxs-lookup"><span data-stu-id="f82a2-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="f82a2-150">_cbEIDContainer で 0 を渡し__、lpEIDContainer で NULL を渡します_。</span><span class="sxs-lookup"><span data-stu-id="f82a2-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="f82a2-151">新しいエントリのエントリ識別子を保持する  _場合は、lppEIDNewEntry_ パラメーターに有効なポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="f82a2-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f82a2-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="f82a2-152">See also</span></span>



[<span data-ttu-id="f82a2-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f82a2-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="f82a2-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f82a2-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="f82a2-155">PidTagCreateTemplates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f82a2-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="f82a2-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f82a2-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

