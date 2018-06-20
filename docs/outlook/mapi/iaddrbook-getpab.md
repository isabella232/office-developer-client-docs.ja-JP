---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800389"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="466d1-103">られたユーザーのプライマリ</span><span class="sxs-lookup"><span data-stu-id="466d1-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="466d1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="466d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="466d1-105">個人用アドレス帳 (PAB) として指定されているコンテナーのエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="466d1-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="466d1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="466d1-106">Parameters</span></span>

 <span data-ttu-id="466d1-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="466d1-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="466d1-108">[out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="466d1-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="466d1-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="466d1-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="466d1-110">[out]個人アドレス帳のエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="466d1-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="466d1-111">_LppEntryID_パラメーターには、コンテナーが、個人用アドレス帳として指定されてない場合は 0 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="466d1-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="466d1-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="466d1-112">Return value</span></span>

<span data-ttu-id="466d1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="466d1-113">S_OK</span></span> 
  
> <span data-ttu-id="466d1-114">個人アドレス帳のエントリ id が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="466d1-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="466d1-115">備考</span><span class="sxs-lookup"><span data-stu-id="466d1-115">Remarks</span></span>

<span data-ttu-id="466d1-116">クライアントは、個人用アドレス帳として指定されているコンテナーのエントリの識別子を取得するために**GetPAB**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="466d1-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="466d1-117">場合は、プロファイルに個人用アドレス帳が確立されていない、MAPI、個人用アドレス帳として最初のコンテナーの選択、アドレス帳階層の変更を可能にします。</span><span class="sxs-lookup"><span data-stu-id="466d1-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="466d1-118">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="466d1-118">MFCMAPI reference</span></span>

<span data-ttu-id="466d1-119">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="466d1-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="466d1-120">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="466d1-120">**File**</span></span>|<span data-ttu-id="466d1-121">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="466d1-121">**Function**</span></span>|<span data-ttu-id="466d1-122">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="466d1-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="466d1-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="466d1-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="466d1-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="466d1-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="466d1-125">MFCMAPI では、 **GetPAB**メソッドを使用して、ユーザーの個人用アドレス帳の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="466d1-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="466d1-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="466d1-126">See also</span></span>



[<span data-ttu-id="466d1-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="466d1-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="466d1-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="466d1-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="466d1-129">PidTagContainerFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="466d1-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="466d1-130">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="466d1-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="466d1-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="466d1-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

