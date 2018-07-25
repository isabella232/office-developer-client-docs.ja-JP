---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog function [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798889"
---
# <a name="fshowdialog"></a><span data-ttu-id="ec50d-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="ec50d-104">fShowDialog</span></span>

 <span data-ttu-id="ec50d-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ec50d-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ec50d-p101">ネイティブ Windows ダイアログ ボックスの例を読み込んで表示するユーザー定義コマンドの例です。GENERIC.xll が読み込まれるとき、このコマンドにアクセスするユーザー定義メニュー [Generic] を作成します。</span><span class="sxs-lookup"><span data-stu-id="ec50d-p101">Example user-defined command that loads and displays an example native Windows dialog box. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="ec50d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ec50d-108">Parameters</span></span>

<span data-ttu-id="ec50d-109">この関数にはパラメーターはありません。</span><span class="sxs-lookup"><span data-stu-id="ec50d-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ec50d-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="ec50d-110">Property Value/Return Value</span></span>

<span data-ttu-id="ec50d-111">この関数は、正常に完了したことを示す整数値 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="ec50d-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec50d-112">注釈</span><span class="sxs-lookup"><span data-stu-id="ec50d-112">Remarks</span></span>

<span data-ttu-id="ec50d-113">ネイティブ Windows ダイアログ ボックスを表示する手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ec50d-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="ec50d-114">**GetHwnd** を使用して、Microsoft Excel メイン ウィンドウ ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec50d-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="ec50d-115">**HookExcelWindow** を使用して Excel メイン ウィンドウをフックします。</span><span class="sxs-lookup"><span data-stu-id="ec50d-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="ec50d-116">**DialogBox** を使用してダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="ec50d-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="ec50d-117">**UnhookExcelWindow** を使用して Excel メイン ウィンドウのフックを解除します。</span><span class="sxs-lookup"><span data-stu-id="ec50d-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="ec50d-118">例</span><span class="sxs-lookup"><span data-stu-id="ec50d-118">Example</span></span>

<span data-ttu-id="ec50d-119">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec50d-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec50d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec50d-120">See also</span></span>



[<span data-ttu-id="ec50d-121">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="ec50d-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

