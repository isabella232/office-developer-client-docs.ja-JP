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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e4bce7f122522532023d18b43fe4bfdeda84af9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800045"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="10c66-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="10c66-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="10c66-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10c66-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10c66-105">プライベート Mapi32.dll へのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="10c66-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="10c66-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="10c66-106">Parameters</span></span>

 <span data-ttu-id="10c66-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="10c66-107">_szComponent_</span></span>
  
> <span data-ttu-id="10c66-108">[in][Mapi32.dll スタブのレジストリ設定](http://msdn.microsoft.com/en-us/library/dd162409.aspx)」で説明する MSIComponentID レジストリ キーです。</span><span class="sxs-lookup"><span data-stu-id="10c66-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/en-us/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="10c66-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="10c66-109">_szQualifier_</span></span>
  
> <span data-ttu-id="10c66-110">[in]MSIApplicationLCID または MSIOfficeLCID のサブキーを[特定のバージョンの MAPI 負荷を選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)」に記載します。</span><span class="sxs-lookup"><span data-stu-id="10c66-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="10c66-111">修飾子がない場合、呼び出し元が**null**渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="10c66-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="10c66-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="10c66-112">_szDllPath_</span></span>
  
> <span data-ttu-id="10c66-113">[in]プライベートの Mapi32.dll は、すべての MAPI 機能 (、Mapi32.dll と同じエクスポート) を持つへのパス。</span><span class="sxs-lookup"><span data-stu-id="10c66-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="10c66-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="10c66-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="10c66-115">[in]_SzDllPath_、文字のサイズです。</span><span class="sxs-lookup"><span data-stu-id="10c66-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="10c66-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="10c66-116">_fInstall_</span></span>
  
> <span data-ttu-id="10c66-117">[in]それが存在しない場合は、プライベート、Mapi32.dll コンポーネントをインストールするのには MAPI を指示します。</span><span class="sxs-lookup"><span data-stu-id="10c66-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10c66-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="10c66-118">Return value</span></span>

 <span data-ttu-id="10c66-119">**true**</span><span class="sxs-lookup"><span data-stu-id="10c66-119">**true**</span></span>
  
> <span data-ttu-id="10c66-120">パスが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="10c66-120">The path was found.</span></span>
    
 <span data-ttu-id="10c66-121">**false**</span><span class="sxs-lookup"><span data-stu-id="10c66-121">**false**</span></span>
  
> <span data-ttu-id="10c66-122">パスが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="10c66-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10c66-123">注釈</span><span class="sxs-lookup"><span data-stu-id="10c66-123">Remarks</span></span>

<span data-ttu-id="10c66-124">プライベート Mapi32.dll へのパスを取得したい場合に、 **FGetComponentPath**関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="10c66-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10c66-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="10c66-125">See also</span></span>



[<span data-ttu-id="10c66-126">読み込む MAPI の特定のバージョンを選択する</span><span class="sxs-lookup"><span data-stu-id="10c66-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="10c66-127">Mapi32.dll スタブのレジストリ設定</span><span class="sxs-lookup"><span data-stu-id="10c66-127">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

