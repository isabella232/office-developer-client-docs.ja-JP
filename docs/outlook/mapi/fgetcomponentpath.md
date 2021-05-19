---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335211"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="12d0a-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="12d0a-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="12d0a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12d0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12d0a-105">プライベート ファイルへのパスを返Mapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="12d0a-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="12d0a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="12d0a-106">Parameters</span></span>

 <span data-ttu-id="12d0a-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="12d0a-107">_szComponent_</span></span>
  
> <span data-ttu-id="12d0a-108">[in]MSIComponentID reg キーは、スタブ レジストリMapi32.dll[で説明](https://msdn.microsoft.com/library/dd162409.aspx)設定。</span><span class="sxs-lookup"><span data-stu-id="12d0a-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="12d0a-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="12d0a-109">_szQualifier_</span></span>
  
> <span data-ttu-id="12d0a-110">[in]「読み込む MAPI の特定のバージョンを選択する」で説明されている MSIApplicationLCID または MSIOfficeLCID [サブキー](how-to-choose-a-specific-version-of-mapi-to-load.md)。</span><span class="sxs-lookup"><span data-stu-id="12d0a-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="12d0a-111">修飾子がない場合、 **呼** び出し元は null を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="12d0a-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="12d0a-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="12d0a-112">_szDllPath_</span></span>
  
> <span data-ttu-id="12d0a-113">[in]MAPI の完全な機能をMapi32.dllプライベート インターフェイスへのパス (エクスポートと同じ) Mapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="12d0a-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="12d0a-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="12d0a-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="12d0a-115">[in]  _szDllPath のサイズ_(文字)。</span><span class="sxs-lookup"><span data-stu-id="12d0a-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="12d0a-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="12d0a-116">_fInstall_</span></span>
  
> <span data-ttu-id="12d0a-117">[in]プライベート コンポーネントが存在しない場合Mapi32.dll MAPI にインストールを指示します。</span><span class="sxs-lookup"><span data-stu-id="12d0a-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12d0a-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="12d0a-118">Return value</span></span>

 <span data-ttu-id="12d0a-119">**true**</span><span class="sxs-lookup"><span data-stu-id="12d0a-119">**true**</span></span>
  
> <span data-ttu-id="12d0a-120">パスが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="12d0a-120">The path was found.</span></span>
    
 <span data-ttu-id="12d0a-121">**false**</span><span class="sxs-lookup"><span data-stu-id="12d0a-121">**false**</span></span>
  
> <span data-ttu-id="12d0a-122">パスが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="12d0a-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12d0a-123">注釈</span><span class="sxs-lookup"><span data-stu-id="12d0a-123">Remarks</span></span>

<span data-ttu-id="12d0a-124">プライベート コンポーネントへのパスを取得する必要がある場合は **、FGetComponentPath** 関数を使用Mapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="12d0a-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12d0a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="12d0a-125">See also</span></span>



[<span data-ttu-id="12d0a-126">読み込む MAPI の特定のバージョンを選択する</span><span class="sxs-lookup"><span data-stu-id="12d0a-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="12d0a-127">Mapi32.dllスタブ レジストリ 設定</span><span class="sxs-lookup"><span data-stu-id="12d0a-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

