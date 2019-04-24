---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd function [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303991"
---
# <a name="xlautoadd"></a><span data-ttu-id="fd6c1-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="fd6c1-104">xlAutoAdd</span></span>

 <span data-ttu-id="fd6c1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fd6c1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fd6c1-p101">ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL をアクティブ化するたびに、Microsoft Excel によって追加されます。Excel が起動して、あらかじめインストールされたアドインを読み込む際には、この関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-p101">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager. This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="fd6c1-108">たとえば、この関数を使用して、アドインが有効になっていることをユーザーに通知するカスタム ダイアログ ボックスの表示、レジストリの読み取りと書き込み、ライセンス情報の確認などができます。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="fd6c1-109">Excel では、これらの関数の実装とエクスポートに XLL は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="fd6c1-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fd6c1-110">Parameters</span></span>

<span data-ttu-id="fd6c1-111">この関数に引数はありません。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fd6c1-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="fd6c1-112">Property value/Return value</span></span>

<span data-ttu-id="fd6c1-113">この関数を実装する場合、1 を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="fd6c1-114">(**int**)。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd6c1-115">注釈</span><span class="sxs-lookup"><span data-stu-id="fd6c1-115">Remarks</span></span>

<span data-ttu-id="fd6c1-116">アドイン マネージャーが任意のタスクを追加するときに、そのタスクを XLL が実行する必要がある場合は、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="fd6c1-117">例</span><span class="sxs-lookup"><span data-stu-id="fd6c1-117">Example</span></span>

<span data-ttu-id="fd6c1-p103">この関数の実装例については、`\SAMPLES\EXAMPLE\EXAMPLE.C` と `\SAMPLES\GENERIC\GENERIC.C` を参照してください。次のコードは、`\SAMPLES\EXAMPLE\EXAMPLE.C` から抜粋しています。</span><span class="sxs-lookup"><span data-stu-id="fd6c1-p103">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function. The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="fd6c1-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd6c1-120">See also</span></span>



[<span data-ttu-id="fd6c1-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="fd6c1-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="fd6c1-122">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="fd6c1-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

