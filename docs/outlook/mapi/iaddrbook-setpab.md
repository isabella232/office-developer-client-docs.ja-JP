---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 461b59ff4f4c8a93f3a9945b05e31aef9a2997bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569303"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="f8d19-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="f8d19-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="f8d19-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8d19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8d19-105">個人用アドレス帳 (PAB) には、特定のコンテナーを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8d19-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="f8d19-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8d19-106">Parameters</span></span>

 <span data-ttu-id="f8d19-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8d19-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f8d19-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="f8d19-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f8d19-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8d19-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f8d19-110">[in]個人アドレス帳として指定するコンテナーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f8d19-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="f8d19-111">_LpEntryID_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f8d19-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8d19-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f8d19-112">Return value</span></span>

<span data-ttu-id="f8d19-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8d19-113">S_OK</span></span> 
  
> <span data-ttu-id="f8d19-114">指定したコンテナーは、個人用アドレス帳として確立されています。</span><span class="sxs-lookup"><span data-stu-id="f8d19-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8d19-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f8d19-115">Remarks</span></span>

<span data-ttu-id="f8d19-116">クライアントとサービス ・ プロバイダーとして、個人用アドレス帳の特定のコンテナーを指定するのには**SetPAB**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8d19-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="f8d19-117">個人アドレス帳は、他のコンテナーと同様に新しいエントリからコピーしたエントリで構成されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f8d19-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="f8d19-118">**SetPAB**への呼び出しは、そのコンテナーが使用できなくなった、または、 **SetPAB**への後続の呼び出しで個人用アドレス帳を新しいコンテナーになりますまで、個人用アドレス帳としてコンテナーを確立します。</span><span class="sxs-lookup"><span data-stu-id="f8d19-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="f8d19-119">クライアントとプロバイダーがありませんに個人用アドレス帳の変更を永続的な[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8d19-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8d19-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="f8d19-120">MFCMAPI reference</span></span>

<span data-ttu-id="f8d19-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f8d19-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8d19-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="f8d19-122">**File**</span></span>|<span data-ttu-id="f8d19-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="f8d19-123">**Function**</span></span>|<span data-ttu-id="f8d19-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="f8d19-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8d19-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f8d19-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="f8d19-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="f8d19-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="f8d19-127">MFCMAPI では、 **SetPAB**メソッドを使用して、指定したコンテナーに、個人用アドレス帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8d19-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8d19-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8d19-128">See also</span></span>



[<span data-ttu-id="f8d19-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="f8d19-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="f8d19-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="f8d19-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="f8d19-131">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8d19-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="f8d19-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f8d19-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="f8d19-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f8d19-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

