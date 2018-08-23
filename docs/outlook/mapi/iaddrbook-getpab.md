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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800389"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="ac0f0-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="ac0f0-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="ac0f0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac0f0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac0f0-105">個人用アドレス帳 (PAB) として指定されているコンテナーのエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ac0f0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ac0f0-106">Parameters</span></span>

 <span data-ttu-id="ac0f0-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac0f0-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="ac0f0-108">[out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ac0f0-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac0f0-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="ac0f0-110">[out]個人アドレス帳のエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="ac0f0-111">_LppEntryID_パラメーターには、コンテナーが、個人用アドレス帳として指定されてない場合は 0 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac0f0-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ac0f0-112">Return value</span></span>

<span data-ttu-id="ac0f0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac0f0-113">S_OK</span></span> 
  
> <span data-ttu-id="ac0f0-114">個人アドレス帳のエントリ id が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac0f0-115">注釈</span><span class="sxs-lookup"><span data-stu-id="ac0f0-115">Remarks</span></span>

<span data-ttu-id="ac0f0-116">クライアントは、個人用アドレス帳として指定されているコンテナーのエントリの識別子を取得するために**GetPAB**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="ac0f0-117">場合は、プロファイルに個人用アドレス帳が確立されていない、MAPI、個人用アドレス帳として最初のコンテナーの選択、アドレス帳階層の変更を可能にします。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac0f0-118">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ac0f0-118">MFCMAPI reference</span></span>

<span data-ttu-id="ac0f0-119">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ac0f0-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac0f0-120">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ac0f0-120">**File**</span></span>|<span data-ttu-id="ac0f0-121">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ac0f0-121">**Function**</span></span>|<span data-ttu-id="ac0f0-122">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ac0f0-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac0f0-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ac0f0-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="ac0f0-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="ac0f0-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="ac0f0-125">MFCMAPI では、 **GetPAB**メソッドを使用して、ユーザーの個人用アドレス帳の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ac0f0-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac0f0-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac0f0-126">See also</span></span>



[<span data-ttu-id="ac0f0-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ac0f0-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ac0f0-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ac0f0-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ac0f0-129">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac0f0-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="ac0f0-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac0f0-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="ac0f0-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ac0f0-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

