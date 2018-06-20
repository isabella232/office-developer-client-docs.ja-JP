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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800383"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="2e9fd-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="2e9fd-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="2e9fd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e9fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e9fd-105">初期のアドレス帳コンテナーのエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="2e9fd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2e9fd-106">Parameters</span></span>

 <span data-ttu-id="2e9fd-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2e9fd-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="2e9fd-108">[out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2e9fd-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="2e9fd-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="2e9fd-110">[out]既定のコンテナーのエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e9fd-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2e9fd-111">Return value</span></span>

<span data-ttu-id="2e9fd-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e9fd-112">S_OK</span></span> 
  
> <span data-ttu-id="2e9fd-113">既定のコンテナーのエントリ id が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e9fd-114">備考</span><span class="sxs-lookup"><span data-stu-id="2e9fd-114">Remarks</span></span>

<span data-ttu-id="2e9fd-115">クライアント アプリケーションとサービス ・ プロバイダーは、既定のアドレス帳コンテナーのエントリの識別子を取得するために**GetDefaultDir**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="2e9fd-116">既定のコンテナーは、どのようなユーザーに表示されるアドレス帳を最初に開いたときに、アドレス帳に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="2e9fd-117">[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドを呼び出すことで、既定のコンテナーが設定されていない場合は、MAPI は個人用アドレス帳 (PAB) ではない名前を持つ最初のコンテナーをデフォルトのコンテナーとして割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="2e9fd-118">このようなコンテナーが見つからない場合、個人用アドレス帳が既定のコンテナーになります。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="2e9fd-119">既定値を設定するのには、ディレクトリ、クライアント、またはプロバイダーは、 **SetDefaultDir**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="2e9fd-120">クライアントとプロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことはありません。アドレス帳への変更は処理されません、ため変更はすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2e9fd-121">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="2e9fd-121">MFCMAPI reference</span></span>

<span data-ttu-id="2e9fd-122">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="2e9fd-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2e9fd-123">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="2e9fd-123">**File**</span></span>|<span data-ttu-id="2e9fd-124">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="2e9fd-124">**Function**</span></span>|<span data-ttu-id="2e9fd-125">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="2e9fd-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e9fd-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2e9fd-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="2e9fd-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="2e9fd-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="2e9fd-128">MFCMAPI では、 **GetDefaultDir**メソッドを使用して、既定のアドレス帳コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e9fd-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e9fd-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e9fd-129">See also</span></span>



[<span data-ttu-id="2e9fd-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="2e9fd-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="2e9fd-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2e9fd-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2e9fd-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2e9fd-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2e9fd-133">PidTagContainerFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="2e9fd-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="2e9fd-134">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2e9fd-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="2e9fd-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2e9fd-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

