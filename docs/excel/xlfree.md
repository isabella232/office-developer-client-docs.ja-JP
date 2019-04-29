---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- xlfree function [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424715"
---
# <a name="xlfree"></a>xlFree

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
[Excel4](excel4-excel12.md)、[Excel4v](excel4v-excel12v.md)、[Excel12](excel4-excel12.md)、または [Excel12v](excel4v-excel12v.md) の呼び出しで戻り値 **XLOPER**/ **XLOPER12** を作成するときに、Microsoft Excel が割り当てたメモリ リソースを解放するために使用します。**xlFree** 関数は補助メモリを解放し、ポインターを **NULL** にリセットしますが、**XLOPER**/ **XLOPER12** の他の部分は破棄しません。
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>パラメーター

 _px_1, ..., px_n_
  
解放する 1 つ以上の **XLOPER**/ **XLOPER12**。Excel 2003 までのバージョンでは、渡せるポインターの最大数は 30 です。Excel 2007 以降は、255 に増加されました。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は値を返しません。
  
## <a name="remarks"></a>注釈

**Excel4** または **Excel4v** から戻り値として取得した **XLOPER**、および **Excel12** または **Excel12v** から戻り値として取得した **XLOPER12** は、型が **xltypeStr**、**xltypeMulti**、または **xltypeRef** のいずれかの場合はすべて解放する必要があります。他の型を解放しても、それが **Excel4** または **Excel12** から取得したものである限り、たとえそれが補助メモリを使用しない場合でも、問題が生じることはありません。
  
解放対象の Excel が割り当てたメモリを含む **XLOPER**/ **XLOPER12** へのポインターを Excel に戻す場合、**xlbitXLFree** を設定して Excel にメモリを確実に解放させます。 
  
## <a name="example"></a>例

この例では **GET.WORKSPACE(1)** を呼び出し、Excel を実行中のプラットフォームを文字列として返します。コードは返された文字列を後で使用するためにバッファーにコピーします。コードはこのバッファーを後で Excel 関数で使用するために **XLOPER12** に戻します。最後に、コードは警告ボックスに文字列を表示します。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>関連項目

- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

