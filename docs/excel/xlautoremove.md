---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlautoremove function [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425478"
---
# <a name="xlautoremove"></a><span data-ttu-id="ab112-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="ab112-104">xlAutoRemove</span></span>

 <span data-ttu-id="ab112-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ab112-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ab112-p101">ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL を非アクティブ化すると、Excel によって呼び出されます。アドインがインストールされている状態で Excel セッションが終了するときには、正常終了でも異常終了でも、この関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="ab112-p101">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager. This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="ab112-108">たとえばこの関数を使用して、アドインが無効になっていることをユーザーに通知するカスタム ダイアログ ボックスを表示したり、レジストリの読み取りと書き込みを行ったりすることができます。</span><span class="sxs-lookup"><span data-stu-id="ab112-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="ab112-109">Excel では、これらの関数の実装とエクスポートに XLL は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ab112-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="ab112-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab112-110">Parameters</span></span>

<span data-ttu-id="ab112-111">この関数に引数はありません。</span><span class="sxs-lookup"><span data-stu-id="ab112-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ab112-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="ab112-112">Property value/Return value</span></span>

<span data-ttu-id="ab112-113">この関数を実装する場合、1 (**int**) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab112-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab112-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ab112-114">Remarks</span></span>

<span data-ttu-id="ab112-115">アドイン マネージャーによってタスクが削除されたときに XLL がそのタスクを完了する必要がある場合は、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab112-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="ab112-116">例</span><span class="sxs-lookup"><span data-stu-id="ab112-116">Example</span></span>

<span data-ttu-id="ab112-p102">この関数の実装例については、`\SAMPLES\EXAMPLE\EXAMPLE.C` ファイルと `\SAMPLES\GENERIC\GENERIC.C` ファイルを参照してください。次のコードは、`\SAMPLES\EXAMPLE\EXAMPLE.C` から抜粋しています。</span><span class="sxs-lookup"><span data-stu-id="ab112-p102">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function. The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ab112-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab112-119">See also</span></span>



[<span data-ttu-id="ab112-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="ab112-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="ab112-121">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="ab112-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

