---
title: 配布リストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333027"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="2914f-103">配布リストの作成</span><span class="sxs-lookup"><span data-stu-id="2914f-103">Creating a distribution list</span></span>

<span data-ttu-id="2914f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2914f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2914f-105">クライアントは、個人用アドレス帳 (PAB) などの変更可能なコンテナーに配布リストを直接作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2914f-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="2914f-106">**PAB で配布リストを作成するには**</span><span class="sxs-lookup"><span data-stu-id="2914f-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="2914f-107">次のように、 **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) という1つのプロパティタグを持つサイズ付きプロパティタグ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="2914f-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="2914f-108">[IAddrBook:: getpab](iaddrbook-getpab.md)を呼び出して、pab のエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="2914f-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="2914f-109">エラーが発生した場合、または**getpab**が0または NULL を返した場合は続行しません。</span><span class="sxs-lookup"><span data-stu-id="2914f-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="2914f-110">[IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出して、PAB を開きます。</span><span class="sxs-lookup"><span data-stu-id="2914f-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="2914f-111">_ulobjtype_出力パラメーターは、MAPI_ABCONT に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2914f-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="2914f-112">PAB の[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、配布リストを作成するために使用するテンプレートである PR_DEF_CREATE_DL プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="2914f-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="2914f-113">**GetProps**が失敗した場合:</span><span class="sxs-lookup"><span data-stu-id="2914f-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="2914f-114">PAB の[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IMAPITable**インターフェイスを持つ**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="2914f-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="2914f-115">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列が "mapipdl" に等しい行を検索するプロパティ制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="2914f-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="2914f-116">この行を検索するには、 [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2914f-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="2914f-117">**GetProps**または**FindRow**のどちらかによって返されるエントリ識別子を保存します。</span><span class="sxs-lookup"><span data-stu-id="2914f-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="2914f-118">PAB の[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出して、保存したエントリ id で表されるテンプレートを使用して新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="2914f-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="2914f-119">この呼び出しがリモートである場合、返されるオブジェクトがメッセージングユーザーではなく配布リストであると仮定してはなりません。</span><span class="sxs-lookup"><span data-stu-id="2914f-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="2914f-120">CREATE_CHECK_DUP フラグは_ulflags_パラメーターで渡されるため、エントリが2回追加されることはありません。</span><span class="sxs-lookup"><span data-stu-id="2914f-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="2914f-121">新しいエントリの**IUnknown:: QueryInterface**メソッドを呼び出して、IID_IDistList をインターフェイス識別子として渡し、エントリが配布リストであるかどうかを確認し、 [IMAPIContainer](idistlistimapicontainer.md)インターフェイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2914f-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="2914f-122">**createentry**は、より具体的な**imailuser**または**imailuser**ポインターではなく**imapiprop**ポインターを返すので、配布リストオブジェクトが作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="2914f-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="2914f-123">**QueryInterface**が成功した場合は、メッセージングユーザーではなく、配布リストが作成されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="2914f-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="2914f-124">配布リストの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、表示名とその他のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2914f-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="2914f-125">配布リストの[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出して、1つまたは複数のメッセージングユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="2914f-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="2914f-126">保存する準備ができたら、配布リストの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2914f-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="2914f-127">保存されている配布リストのエントリ識別子を取得するには、KEEP_OPEN_READWRITE フラグを設定してから、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求する[imapiprop:: GetProps](imapiprop-getprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2914f-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="2914f-128">**IUnknown:: release**メソッドを呼び出して、新しい配布リストと PAB を解放します。</span><span class="sxs-lookup"><span data-stu-id="2914f-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="2914f-129">[MAPIFreeBuffer](mapifreebuffer.md)を呼び出して、PAB のエントリ識別子とサイズ付きプロパティタグ配列のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="2914f-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

