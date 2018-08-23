---
title: 配布リストを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f0a6b7af196073d52ce98037b443569dcd1f41e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582547"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="7ceef-103">配布リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-103">Creating a distribution list</span></span>

<span data-ttu-id="7ceef-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ceef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ceef-105">クライアントは、個人用アドレス帳 (PAB) などの変更可能なコンテナーに直接配布リストを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="7ceef-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="7ceef-106">**個人アドレス帳の配布リストを作成するには**</span><span class="sxs-lookup"><span data-stu-id="7ceef-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="7ceef-107">プロパティを 1 つのタグ、 **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) で次のようにサイズのプロパティ タグ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="7ceef-108">個人アドレス帳のエントリ id を取得するために[られたユーザーのプライマリ](iaddrbook-getpab.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="7ceef-109">エラーが発生、または**GetPAB**には、0 または NULL が返されますが続行されません。</span><span class="sxs-lookup"><span data-stu-id="7ceef-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="7ceef-110">開くには、個人用アドレス帳[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="7ceef-111">_UlObjType_の出力パラメーターは、MAPI_ABCONT に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ceef-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="7ceef-112">PR_DEF_CREATE_DL プロパティを使用して、配布リストを作成するテンプレートを取得するために、個人用アドレス帳の[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="7ceef-113">**GetProps**が失敗した場合。</span><span class="sxs-lookup"><span data-stu-id="7ceef-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="7ceef-114">**IMAPITable**インターフェイスを使用して**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを開くには、個人用アドレス帳の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="7ceef-115">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) の列が"MAPIPDL"にします行を検索するプロパティ条件を作成します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="7ceef-116">この行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="7ceef-117">**GetProps**または**FindRow**のいずれかによって返されるエントリの識別子を保存します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="7ceef-118">保存されたエントリの識別子によって表されたテンプレートを使用して新しいエントリを作成するのには、個人用アドレス帳の[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="7ceef-119">返されるオブジェクトされるメッセージングのユーザーではなく、配布リストと、この呼び出しはリモートとは限りません。</span><span class="sxs-lookup"><span data-stu-id="7ceef-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="7ceef-120">_UlFlags_パラメーター エントリが 2 回追加されることを防ぐために CREATE_CHECK_DUP フラグが渡されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7ceef-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="7ceef-121">IID_IDistList を渡すことを確認エントリ、配布リストをサポートするのには、インターフェイス識別子と、新しいエントリの**IUnknown::QueryInterface**メソッドを呼び出して、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="7ceef-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="7ceef-122">**CreateEntry**は、特定の**IMailUser**または**IDistList**のポインターではなく、 **IMAPIProp**ポインターを返す、ために、配布リスト オブジェクトが作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="7ceef-123">**QueryInterface**が成功した場合、メッセージングのユーザーではなく、配布リストが作成されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ceef-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="7ceef-124">表示名およびその他のプロパティを設定するのには、配布リストの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="7ceef-125">1 つまたは複数のメッセージングのユーザーを追加するのには、配布リストの[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="7ceef-126">保存する準備ができたら、配布リストの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="7ceef-127">保存されている配布リストのエントリの識別子を取得するには、KEEP_OPEN_READWRITE フラグを設定し、 [IMAPIProp::GetProps](imapiprop-getprops.md) ([PidTagEntryId](pidtagentryid-canonical-property.md)) の**PR_ENTRYID**プロパティを要求するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="7ceef-128">**** メソッドを呼び出すことによって新しい配布リストと、個人用アドレス帳を解放します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="7ceef-129">個人用アドレス帳およびサイズのプロパティ タグ配列のエントリの識別子のメモリを解放するのには[MAPIFreeBuffer](mapifreebuffer.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ceef-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

