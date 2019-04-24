---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336695"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="81c90-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="81c90-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="81c90-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81c90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81c90-105">最初のアドレス帳コンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="81c90-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="81c90-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81c90-106">Parameters</span></span>

 <span data-ttu-id="81c90-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="81c90-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="81c90-108">読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="81c90-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="81c90-109">_lppentryid_</span><span class="sxs-lookup"><span data-stu-id="81c90-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="81c90-110">読み上げ既定のコンテナーのエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="81c90-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81c90-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="81c90-111">Return value</span></span>

<span data-ttu-id="81c90-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="81c90-112">S_OK</span></span> 
  
> <span data-ttu-id="81c90-113">既定のコンテナーのエントリ識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="81c90-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81c90-114">解説</span><span class="sxs-lookup"><span data-stu-id="81c90-114">Remarks</span></span>

<span data-ttu-id="81c90-115">クライアントアプリケーションおよびサービスプロバイダーは、 **GetDefaultDir**メソッドを呼び出して、既定のアドレス帳コンテナーのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="81c90-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="81c90-116">既定のコンテナーは、アドレス帳が最初に開かれたときに、ユーザーにアドレス帳で表示されることを示します。</span><span class="sxs-lookup"><span data-stu-id="81c90-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="81c90-117">[IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドの呼び出しによって既定のコンテナーが設定されていない場合、MAPI は、個人用アドレス帳 (PAB) ではない名前の最初のコンテナーを既定のコンテナーとして割り当てます。</span><span class="sxs-lookup"><span data-stu-id="81c90-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="81c90-118">このようなコンテナーが見つからない場合、PAB は既定のコンテナーになります。</span><span class="sxs-lookup"><span data-stu-id="81c90-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="81c90-119">既定のディレクトリを設定するために、クライアントまたはプロバイダーは**SetDefaultDir**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="81c90-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="81c90-120">クライアントとプロバイダーは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要はありません。アドレス帳への変更は処理されないため、変更はすぐに永続的に加えられます。</span><span class="sxs-lookup"><span data-stu-id="81c90-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="81c90-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="81c90-121">MFCMAPI reference</span></span>

<span data-ttu-id="81c90-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81c90-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="81c90-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="81c90-123">**File**</span></span>|<span data-ttu-id="81c90-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="81c90-124">**Function**</span></span>|<span data-ttu-id="81c90-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="81c90-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81c90-126">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="81c90-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="81c90-127">CMainDlg:: OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="81c90-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="81c90-128">mfcmapi は、 **GetDefaultDir**メソッドを使用して、既定のアドレス帳コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="81c90-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81c90-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="81c90-129">See also</span></span>



[<span data-ttu-id="81c90-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="81c90-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="81c90-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="81c90-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="81c90-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="81c90-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="81c90-133">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="81c90-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="81c90-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="81c90-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="81c90-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="81c90-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

