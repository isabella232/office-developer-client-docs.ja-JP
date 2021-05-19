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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424176"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="18344-103">配布リストの作成</span><span class="sxs-lookup"><span data-stu-id="18344-103">Creating a distribution list</span></span>

<span data-ttu-id="18344-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18344-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18344-105">クライアントは、個人用アドレス帳 (PAB) などの変更可能なコンテナーに配布リストを直接作成できます。</span><span class="sxs-lookup"><span data-stu-id="18344-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="18344-106">**PAB で配布リストを作成するには**</span><span class="sxs-lookup"><span data-stu-id="18344-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="18344-107">次のように、1 つのプロパティ タグ [(PidTagDefCreateDl)](pidtagdefcreatedl-canonical-property.md)を **PR_DEF_CREATE_DLサイズの** プロパティ タグ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="18344-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="18344-108">[IAddrBook::GetPAB](iaddrbook-getpab.md)を呼び出して、PAB のエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="18344-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="18344-109">エラーが発生した場合、 **または GetPAB** がゼロまたは NULL を返す場合は、続行しない。</span><span class="sxs-lookup"><span data-stu-id="18344-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="18344-110">[IAddrBook::OpenEntry を呼び出して](iaddrbook-openentry.md)PAB を開きます。</span><span class="sxs-lookup"><span data-stu-id="18344-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="18344-111">_ulObjType 出力_ パラメーターは、次の値にMAPI_ABCONT。</span><span class="sxs-lookup"><span data-stu-id="18344-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="18344-112">PAB の [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_DEF_CREATE_DL プロパティ (配布リストの作成に使用するテンプレート) を取得します。</span><span class="sxs-lookup"><span data-stu-id="18344-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="18344-113">**GetProps が失敗** した場合:</span><span class="sxs-lookup"><span data-stu-id="18344-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="18344-114">PAB の [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IMAPITable** インターフェイスで PR_CREATE_TEMPLATES ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開きます。 </span><span class="sxs-lookup"><span data-stu-id="18344-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="18344-115">プロパティの制限を作成して、"MAPIPDL" PR_ADDRTYPE **(** [PidTagAddressType](pidtagaddresstype-canonical-property.md)) 列を使用して行を検索します。</span><span class="sxs-lookup"><span data-stu-id="18344-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="18344-116">[IMAPITable::FindRow を呼び出して](imapitable-findrow.md)、この行を探します。</span><span class="sxs-lookup"><span data-stu-id="18344-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="18344-117">**GetProps** または FindRow によって返されるエントリ識別子 **を保存します**。</span><span class="sxs-lookup"><span data-stu-id="18344-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="18344-118">PAB の [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、保存されたエントリ識別子で表されるテンプレートを使用して新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="18344-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="18344-119">この呼び出しがリモートで行う場合、返されるオブジェクトがメッセージング ユーザーではなく配布リストになるとは想定されません。</span><span class="sxs-lookup"><span data-stu-id="18344-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="18344-120">エントリが 2 回CREATE_CHECK_DUPされるのを防ぐために  _、ulFlags_ パラメーターに CREATE_CHECK_DUP フラグが渡されます。</span><span class="sxs-lookup"><span data-stu-id="18344-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="18344-121">新しいエントリの **IUnknown::QueryInterface** メソッドを呼び出し、IID_IDistList をインターフェイス識別子として渡して、エントリが配布リストであり [、IDistList : IMAPIContainer](idistlistimapicontainer.md) インターフェイスをサポートしているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="18344-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="18344-122">**CreateEntry は**、より具体的な **IMailUser** または **IDistList** ポインターではなく **IMAPIProp** ポインターを返すので、配布リスト オブジェクトが作成されたのを確認します。</span><span class="sxs-lookup"><span data-stu-id="18344-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="18344-123">**QueryInterface が** 成功した場合は、メッセージング ユーザーではなく配布リストを作成したと確認できます。</span><span class="sxs-lookup"><span data-stu-id="18344-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="18344-124">配布リストの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、表示名とその他のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="18344-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="18344-125">配布リストの [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、1 つ以上のメッセージング ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="18344-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="18344-126">配布リストを保存する準備ができたら、配布リストの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="18344-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="18344-127">保存された配布リストのエントリ識別子を取得するには、KEEP_OPEN_READWRITE フラグを設定し、PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを要求する [IMAPIProp::GetProps](imapiprop-getprops.md) **を** 呼び出します。</span><span class="sxs-lookup"><span data-stu-id="18344-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="18344-128">**IUnknown::Release** メソッドを呼び出して、新しい配布リストと PAB を解放します。</span><span class="sxs-lookup"><span data-stu-id="18344-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="18344-129">[MAPIFreeBuffer を呼](mapifreebuffer.md)び出して、PAB のエントリ識別子とサイズの大きなプロパティ タグ配列のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="18344-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

