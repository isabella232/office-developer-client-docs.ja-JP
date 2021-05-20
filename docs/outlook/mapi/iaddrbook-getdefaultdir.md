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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436875"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="fd8ca-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="fd8ca-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="fd8ca-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd8ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd8ca-105">最初のアドレス帳コンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="fd8ca-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fd8ca-106">Parameters</span></span>

 <span data-ttu-id="fd8ca-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fd8ca-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="fd8ca-108">[out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="fd8ca-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="fd8ca-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="fd8ca-110">[out]既定のコンテナーのエントリ識別子へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd8ca-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="fd8ca-111">Return value</span></span>

<span data-ttu-id="fd8ca-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd8ca-112">S_OK</span></span> 
  
> <span data-ttu-id="fd8ca-113">既定のコンテナーのエントリ識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd8ca-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fd8ca-114">Remarks</span></span>

<span data-ttu-id="fd8ca-115">クライアント アプリケーションとサービス プロバイダーは **、GetDefaultDir** メソッドを呼び出して、既定のアドレス帳コンテナーのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="fd8ca-116">既定のコンテナーは、ユーザーがアドレス帳を最初に開いたときにアドレス帳に表示されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="fd8ca-117">[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドの呼び出しによって既定のコンテナーが設定されていない場合、MAPI は、個人アドレス帳 (PAB) ではない名前を持つ最初のコンテナーを既定のコンテナーとして割り当てる。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="fd8ca-118">そのようなコンテナーが見つからない場合、PAB は既定のコンテナーになります。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="fd8ca-119">既定のディレクトリを設定するには、クライアントまたはプロバイダーが **SetDefaultDir メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="fd8ca-120">クライアントとプロバイダーは [、IMAPIProp::SaveChanges メソッドを呼び出す必要](imapiprop-savechanges.md) があります。アドレス帳に対する変更は処理されないので、変更は直ちに永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fd8ca-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="fd8ca-121">MFCMAPI reference</span></span>

<span data-ttu-id="fd8ca-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fd8ca-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="fd8ca-123">**File**</span></span>|<span data-ttu-id="fd8ca-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="fd8ca-124">**Function**</span></span>|<span data-ttu-id="fd8ca-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="fd8ca-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd8ca-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="fd8ca-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="fd8ca-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="fd8ca-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="fd8ca-128">MFCMAPI は **GetDefaultDir** メソッドを使用して、既定のアドレス帳コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd8ca-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd8ca-129">See also</span></span>



[<span data-ttu-id="fd8ca-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="fd8ca-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="fd8ca-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="fd8ca-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="fd8ca-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fd8ca-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fd8ca-133">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fd8ca-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="fd8ca-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fd8ca-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="fd8ca-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="fd8ca-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

