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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c20cd7f82df2fb7f878db177fdc940022e1da351
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800382"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="732c0-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="732c0-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="732c0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="732c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="732c0-105">[IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決の処理に含まれるコンテナーのエントリ id の順序付きリストを返します。</span><span class="sxs-lookup"><span data-stu-id="732c0-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="732c0-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="732c0-106">Parameters</span></span>

 <span data-ttu-id="732c0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="732c0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="732c0-108">[in]検索パスで返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="732c0-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="732c0-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="732c0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="732c0-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="732c0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="732c0-111">関数が返す文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="732c0-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="732c0-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="732c0-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="732c0-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="732c0-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="732c0-114">[out]コンテナーのエントリ id の順序付きリストへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="732c0-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="732c0-115">**GetSearchPath** [SRowSet](srowset.md)構造体の順序付きリストを格納します。</span><span class="sxs-lookup"><span data-stu-id="732c0-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="732c0-116">アドレス帳の階層内のコンテナーがない場合、 **SRowSet**構造体で 0 が返されます。</span><span class="sxs-lookup"><span data-stu-id="732c0-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="732c0-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="732c0-117">Return value</span></span>

<span data-ttu-id="732c0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="732c0-118">S_OK</span></span> 
  
> <span data-ttu-id="732c0-119">検索パスが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="732c0-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="732c0-120">注釈</span><span class="sxs-lookup"><span data-stu-id="732c0-120">Remarks</span></span>

<span data-ttu-id="732c0-121">クライアントとサービス ・ プロバイダーは、 **ResolveName**メソッドを使用して名前を解決するために使用される検索パスを取得する**GetSearchPath**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="732c0-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="732c0-122">通常、クライアントは、それを取得するために**GetSearchPath**を呼び出す前に、プロファイルにコンテナーの検索パスを確立するために[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="732c0-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="732c0-123">ただし、 **SetSearchPath**の呼び出しは、省略可能です。</span><span class="sxs-lookup"><span data-stu-id="732c0-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="732c0-124">**SetSearchPath**が呼び出されていない場合**GetSearchPath**パスを構築を通じて、アドレス帳の階層テーブルです。</span><span class="sxs-lookup"><span data-stu-id="732c0-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="732c0-125">**GetSearchPath**によって設定された既定の検索パスは、次の順序で次のコンテナーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="732c0-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="732c0-126">個人用アドレス帳 (PAB) では通常、読み取り/書き込みアクセス許可を持つ最初のコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="732c0-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="732c0-127">その**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) プロパティが DT_GLOBAL に設定されているすべてのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="732c0-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="732c0-128">この設定は、受信者コンテナーを保持していることを示します。</span><span class="sxs-lookup"><span data-stu-id="732c0-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="732c0-129">DT_GLOBAL フラグが、 **PR_DISPLAY_TYPE**プロパティと既定のコンテナーに設定されているコンテナーがない場合、既定値として指定されているコンテナーは、読み取り/書き込みアクセス許可を持つ最初のコンテナーとは異なります。</span><span class="sxs-lookup"><span data-stu-id="732c0-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="732c0-130">**SetSearchPath**が呼び出されると、 **GetSearchPath**は、プロファイルに格納されているアドレス帳コンテナーを使用してパスを作成します。</span><span class="sxs-lookup"><span data-stu-id="732c0-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="732c0-131">**GetSearchPath**は、呼び出し元に返す前に、このパスを検証します。</span><span class="sxs-lookup"><span data-stu-id="732c0-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="732c0-132">**SetSearchPath**の最初の呼び出しの後に、 **GetSearchPath**によって返される検索パスを変更するのには**SetSearchPath**以降の呼び出しを使用してください。</span><span class="sxs-lookup"><span data-stu-id="732c0-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="732c0-133">つまり、呼び出し元のクライアントやプロバイダーは、デフォルトの検索パスを**SetSearchPath**に最初の呼び出し後受信しません。</span><span class="sxs-lookup"><span data-stu-id="732c0-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="732c0-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="732c0-134">See also</span></span>



[<span data-ttu-id="732c0-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="732c0-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="732c0-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="732c0-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="732c0-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="732c0-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

