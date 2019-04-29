---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412983"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="bb8fb-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="bb8fb-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="bb8fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb8fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb8fb-105">[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決プロセスに含まれるコンテナーのエントリ id の順序付きリストを返します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="bb8fb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb8fb-106">Parameters</span></span>

 <span data-ttu-id="bb8fb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb8fb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bb8fb-108">順番検索パスで返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="bb8fb-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-109">The following flag can be set:</span></span>
    
<span data-ttu-id="bb8fb-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bb8fb-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bb8fb-111">返される文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="bb8fb-112">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="bb8fb-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="bb8fb-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="bb8fb-114">読み上げコンテナーエントリ識別子の順序付きリストへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="bb8fb-115">**GetSearchPath**は、注文されたリストを[srowset](srowset.md)構造に格納します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="bb8fb-116">アドレス帳の階層にコンテナーが存在しない場合は、 **srowset**構造体に0が返されます。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bb8fb-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="bb8fb-117">Return value</span></span>

<span data-ttu-id="bb8fb-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb8fb-118">S_OK</span></span> 
  
> <span data-ttu-id="bb8fb-119">検索パスが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb8fb-120">注釈</span><span class="sxs-lookup"><span data-stu-id="bb8fb-120">Remarks</span></span>

<span data-ttu-id="bb8fb-121">クライアントおよびサービスプロバイダーは、 **GetSearchPath**メソッドを呼び出して、 **ResolveName**メソッドで名前を解決するために使用される検索パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="bb8fb-122">通常、クライアントは[IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出して、プロファイルにコンテナー検索パスを設定してから、 **GetSearchPath**を呼び出して取得します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="bb8fb-123">ただし、 **SetSearchPath**の呼び出しはオプションです。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="bb8fb-124">**SetSearchPath**が呼び出されていない場合、 **GetSearchPath**はアドレス帳の階層テーブルを使用してパスを作成します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="bb8fb-125">**GetSearchPath**によって確立される既定の検索パスは、次の順序で構成されています。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="bb8fb-126">読み取り/書き込みアクセス許可を持つ最初のコンテナー。通常は個人用アドレス帳 (PAB)。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="bb8fb-127">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) プロパティが DT_GLOBAL に設定されているすべてのコンテナー。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="bb8fb-128">この設定は、コンテナーが受信者を保持することを示します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="bb8fb-129">**PR_DISPLAY_TYPE**プロパティに DT_GLOBAL フラグが設定されていて、既定のコンテナーが読み取り/書き込みアクセス許可を持つ最初のコンテナーと異なる場合に、既定として指定されているコンテナー。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="bb8fb-130">**SetSearchPath**が呼び出されている場合、 **GetSearchPath**は、プロファイルに格納されているアドレス帳のコンテナーを使用してパスを作成します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="bb8fb-131">**GetSearchPath**は、このパスを呼び出し元に返す前に検証します。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="bb8fb-132">**SetSearchPath**の最初の呼び出しの後、 **SetSearchPath**の以降の呼び出しを使用して、 **GetSearchPath**によって返される検索パスを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="bb8fb-133">言い換えると、呼び出し元のクライアントまたはプロバイダーは、 **SetSearchPath**の最初の呼び出しの後に既定の検索パスを受信しません。</span><span class="sxs-lookup"><span data-stu-id="bb8fb-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb8fb-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb8fb-134">See also</span></span>



[<span data-ttu-id="bb8fb-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="bb8fb-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="bb8fb-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="bb8fb-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="bb8fb-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bb8fb-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

