---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlautoopen function [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798957"
---
# <a name="xlautoopen"></a><span data-ttu-id="37a56-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="37a56-104">xlAutoOpen</span></span>

 <span data-ttu-id="37a56-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37a56-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="37a56-p101">すべての有効な XLL によって実装およびエクスポートされる必要があるコールバック関数。XLL 関数とコマンドの登録、データ構造の初期化、ユーザー インターフェイスのカスタマイズなどを行う場合には、**xlAutoOpen** 関数を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="37a56-p101">Callback function that must be implemented and exported by every valid XLL. The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="37a56-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37a56-108">Parameters</span></span>

<span data-ttu-id="37a56-109">この関数に引数はありません。</span><span class="sxs-lookup"><span data-stu-id="37a56-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="37a56-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="37a56-110">Property Value/Return Value</span></span>

<span data-ttu-id="37a56-111">この関数を実装する場合、1 (**int**) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="37a56-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37a56-112">注釈</span><span class="sxs-lookup"><span data-stu-id="37a56-112">Remarks</span></span>

<span data-ttu-id="37a56-p102">Microsoft Excel は、XLL がアクティブになると常に **xlAutoOpen** を呼び出します。以下の状況で、XLL はアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="37a56-p102">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated. The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="37a56-115">正常終了した前回の Excel セッションでアクティブであった場合、Excel セッションの開始時。</span><span class="sxs-lookup"><span data-stu-id="37a56-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="37a56-116">Excel セッション中に読み込まれた場合。</span><span class="sxs-lookup"><span data-stu-id="37a56-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="37a56-117">XLL は以下のいくつかの方法で読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="37a56-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="37a56-118">**[ファイル]** メニューの **[開く]** を選択する (Excel のバージョンが XLL 読み込みのこの方法をサポートしている場合)。</span><span class="sxs-lookup"><span data-stu-id="37a56-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="37a56-119">アドイン マネージャーを使用する。</span><span class="sxs-lookup"><span data-stu-id="37a56-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="37a56-120">この DLL の名前を唯一の引数として [xlfRegister](xlfregister-form-1.md) を呼び出す別の XLL から。</span><span class="sxs-lookup"><span data-stu-id="37a56-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="37a56-121">この DLL の名前を唯一の引数として [REGISTER](xlfregister-form-1.md) を呼び出す XLM マクロ シートから。</span><span class="sxs-lookup"><span data-stu-id="37a56-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="37a56-122">アドインが、Excel セッション中に非アクティブにされてから再度アクティブにされる場合、この関数は再アクティブ化のときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="37a56-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="37a56-123">例</span><span class="sxs-lookup"><span data-stu-id="37a56-123">Example</span></span>

<span data-ttu-id="37a56-124">この関数の実装例については、`SAMPLES\EXAMPLE\EXAMPLE.C` ファイルと `SAMPLES\GENERIC\GENERIC.C` ファイルをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="37a56-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37a56-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="37a56-125">See also</span></span>



[<span data-ttu-id="37a56-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="37a56-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="37a56-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="37a56-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="37a56-128">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="37a56-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

