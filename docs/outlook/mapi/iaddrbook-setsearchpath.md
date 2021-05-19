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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426206"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="dfc31-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="dfc31-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="dfc31-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc31-105">名前解決プロセスに使用するプロファイル内の新しい検索パスを設定します。</span><span class="sxs-lookup"><span data-stu-id="dfc31-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="dfc31-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dfc31-106">Parameters</span></span>

 <span data-ttu-id="dfc31-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dfc31-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dfc31-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="dfc31-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="dfc31-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="dfc31-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="dfc31-110">[in]検索パスを保持するために使用される [SRowSet](srowset.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dfc31-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="dfc31-111">**SRowSet** の **各 aRow** メンバーの最初のプロパティは、PR_ENTRYID **(** [PidTagEntryId) である必要があります](pidtagentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="dfc31-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfc31-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="dfc31-112">Return value</span></span>

<span data-ttu-id="dfc31-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfc31-113">S_OK</span></span> 
  
> <span data-ttu-id="dfc31-114">検索パスが正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="dfc31-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="dfc31-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="dfc31-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="dfc31-116">**SRowSet** 構造体で説明されているコンテナーの 1 つには、その **プロパティPR_ENTRYID含** めなかった。</span><span class="sxs-lookup"><span data-stu-id="dfc31-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dfc31-117">注釈</span><span class="sxs-lookup"><span data-stu-id="dfc31-117">Remarks</span></span>

<span data-ttu-id="dfc31-118">クライアントとサービス プロバイダーは **、SetSearchPath** メソッドを呼び出して [、IAddrBook::ResolveName](iaddrbook-resolvename.md) メソッドで名前を解決するために使用されるコンテナー検索順序に加えた変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="dfc31-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="dfc31-119">検索パスは、セッションのインスタンス間で保存されます。</span><span class="sxs-lookup"><span data-stu-id="dfc31-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="dfc31-120">クライアントとプロバイダーは、検索パスの変更を永続的に行うために [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfc31-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfc31-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfc31-121">See also</span></span>



[<span data-ttu-id="dfc31-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="dfc31-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="dfc31-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="dfc31-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="dfc31-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="dfc31-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="dfc31-125">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dfc31-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="dfc31-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dfc31-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

