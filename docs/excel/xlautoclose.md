---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- xlautoclose function [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e27ac922c4ba53a30e8e485d3210acc62b7d4bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415860"
---
# <a name="xlautoclose"></a><span data-ttu-id="322e7-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="322e7-104">xlAutoClose</span></span>

 <span data-ttu-id="322e7-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="322e7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="322e7-p101">XLL ファイルが非アクティブになるたびに、Microsoft Excel に呼び出されます。Excel セッションが正常に終了すると、アドインは非アクティブになります。アドインは、Excel セッション中にユーザーによって非アクティブ化される場合があります。この関数はその場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="322e7-p101">Called by Microsoft Excel whenever the XLL is deactivated. The add-in is deactivated when an Excel session ends normally. The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="322e7-p102">関数とコマンドの登録解除、リソースの解放、カスタマイズを元に戻すことなどを XLL が実行できるようするために適切なことではありますが、Excel はこの関数を実装しエクスポートするのに、XLL を必要としません。関数とコマンドを XLL が明示的に登録解除しない場合、**xlAutoClose** 関数を呼び出した後、Excel はこれを実行します。</span><span class="sxs-lookup"><span data-stu-id="322e7-p102">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on. If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="322e7-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="322e7-111">Parameters</span></span>

<span data-ttu-id="322e7-112">この関数に引数はありません。</span><span class="sxs-lookup"><span data-stu-id="322e7-112">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="322e7-113">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="322e7-113">Property value/Return value</span></span>

<span data-ttu-id="322e7-114">この関数を実装する場合、1 (**int**) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="322e7-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="322e7-115">注釈</span><span class="sxs-lookup"><span data-stu-id="322e7-115">Remarks</span></span>

<span data-ttu-id="322e7-p103">XLL が非アクティブになる、つまりメモリからアンロードされるたびに、Excel は **xlAutoClose** 関数を呼び出します。以下の状況で、XLL は非アクティブになります。</span><span class="sxs-lookup"><span data-stu-id="322e7-p103">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory. The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="322e7-118">セッション中にアクティブな場合に、Excel セッションが正常に終了した時点。</span><span class="sxs-lookup"><span data-stu-id="322e7-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="322e7-119">Excel セッション中に明示的にアンロードされた場合。</span><span class="sxs-lookup"><span data-stu-id="322e7-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="322e7-120">XLL は以下のいくつかの方法でアンロードされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="322e7-120">An XLL can be unloaded in several ways:</span></span>
    
- <span data-ttu-id="322e7-121">アドイン マネージャーを使用する。</span><span class="sxs-lookup"><span data-stu-id="322e7-121">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="322e7-122">この DLL の名前を唯一の引数として取る [xlfUnregister](xlfunregister-form-1.md) を呼び出す別の XLL から。</span><span class="sxs-lookup"><span data-stu-id="322e7-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="322e7-123">この DLL の名前を唯一の引数として取る [UNREGISTER](xlfunregister-form-1.md) を呼び出す XLM マクロ シートから。</span><span class="sxs-lookup"><span data-stu-id="322e7-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="322e7-124">この関数は、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="322e7-124">This function should do the following:</span></span>
  
- <span data-ttu-id="322e7-125">XLL が追加した任意のメニューまたはメニュー項目を削除する。</span><span class="sxs-lookup"><span data-stu-id="322e7-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="322e7-126">任意の必要なグローバル クリーンアップを実行する。</span><span class="sxs-lookup"><span data-stu-id="322e7-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="322e7-p104">作成された任意の名前、特にエクスポートされた関数の名前を削除する。**REGISTER** に 4 番目の引数が指定されていると、関数の登録が原因で複数の名前が作成される可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="322e7-p104">Delete any names that were created, especially names of exported functions. Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="322e7-129">例</span><span class="sxs-lookup"><span data-stu-id="322e7-129">Example</span></span>

<span data-ttu-id="322e7-p105">この関数の実装例については、`SAMPLES\EXAMPLE\EXAMPLE.C` ファイルと `SAMPLES\GENERIC\GENERIC.C` ファイルを参照してください。次のコードは、`SAMPLES\GENERIC\GENERIC.C` から抜粋しています。</span><span class="sxs-lookup"><span data-stu-id="322e7-p105">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function. The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="322e7-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="322e7-132">See also</span></span>



[<span data-ttu-id="322e7-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="322e7-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="322e7-134">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="322e7-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

