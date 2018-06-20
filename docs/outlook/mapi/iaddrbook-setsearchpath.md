---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4f9d2f4d271e467d8fac32b8f17faa8f66cd3f99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800395"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="0cf84-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="0cf84-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="0cf84-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0cf84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0cf84-105">名前解決の処理に使用されるプロファイルに新しい検索パスを設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf84-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="0cf84-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="0cf84-106">Parameters</span></span>

 <span data-ttu-id="0cf84-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0cf84-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0cf84-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="0cf84-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0cf84-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="0cf84-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="0cf84-110">[in]検索パスを保持するために使用する[SRowSet](srowset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0cf84-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="0cf84-111">**SRowSet**で**aRow**メンバーごとに、最初のプロパティは、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0cf84-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0cf84-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0cf84-112">Return value</span></span>

<span data-ttu-id="0cf84-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0cf84-113">S_OK</span></span> 
  
> <span data-ttu-id="0cf84-114">検索パスが正しく設定されました。</span><span class="sxs-lookup"><span data-stu-id="0cf84-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="0cf84-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="0cf84-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="0cf84-116">**PR_ENTRYID**プロパティは、 **SRowSet**構造で説明されているコンテナーの 1 つ含まれていません。</span><span class="sxs-lookup"><span data-stu-id="0cf84-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0cf84-117">備考</span><span class="sxs-lookup"><span data-stu-id="0cf84-117">Remarks</span></span>

<span data-ttu-id="0cf84-118">クライアントとサービス ・ プロバイダーは、 [IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドを使用して名前を解決するために使用されるコンテナーの検索順序に加えられた変更を保存する**SetSearchPath**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0cf84-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="0cf84-119">検索パスは、セッションのインスタンス間で保存されます。</span><span class="sxs-lookup"><span data-stu-id="0cf84-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="0cf84-120">クライアントとプロバイダーがありません、検索パスの変更を適用する[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0cf84-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0cf84-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="0cf84-121">See also</span></span>



[<span data-ttu-id="0cf84-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="0cf84-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="0cf84-123">られたユーザーのプライマリ</span><span class="sxs-lookup"><span data-stu-id="0cf84-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="0cf84-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="0cf84-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="0cf84-125">PidTagContainerFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="0cf84-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="0cf84-126">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0cf84-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

