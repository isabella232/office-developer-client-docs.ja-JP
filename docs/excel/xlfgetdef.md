---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421999"
---
# <a name="xlfgetdef"></a>xlfGetDef

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Returns the name, as text, that is defined for a particular area, value, or formula in a workbook. In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition. To get the definition of a name, use [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>パラメーター

_pxDefText_ (**xltypeStr**)
  
参照、値、オブジェクト、数式など、参照先の名前として定義できるあらゆるものを指定できます。
  
参照の場合は、`"R3C5"` などの R1C1 スタイルで指定する必要があります。_pxDefText_ が値または数式の場合、**[名前の管理]** ダイアログ ボックスの **[参照範囲]** 列に表示される等号 (=) を含める必要はありません。_pxDefText_ に複数の名前が存在する場合、**xlfGetDef** は最初の名前を返します。_pxDefText_ に一致する名前がない場合、**xlfGetDef** はエラー値 `#NAME?` を返します。 
  
_pxDocumentText_ (**xltypeStr**)
  
_pxDefText_ が存在するシートを指定します。_pxDocumentText_ が省略されると、アクティブなシートとして想定されます。 
  
_pxTypeNum_ (**xltypeNum**)
  
返す名前の種類を指定する、1 から 3 の範囲の数値です。
  
|**_pxTypeNum_**|**返される値**|
|:-----|:-----|
|1 または省略  <br/> |標準名のみ。  <br/> |
|2   <br/> |非表示名のみ。  <br/> |
|3   <br/> |すべての名前。  <br/> |
   
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 _pxRes_ (**xltypeStr** または **xltypeErr**)
  
指定の定義に関連付けられている名前を返します。
  
## <a name="remarks"></a>注釈

次の表に、特定の引数を指定して **xlfGetDef** を呼び出した場合に返される値の例を 4 つ示します。 
  
|**Excel で定義された名前**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**戻り値**|
|:-----|:-----|:-----|:-----|:-----|
|Sheet4 の指定の範囲には「Sales」という名前が付いています。  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<�ȗ�\>  <br/> |"Sales"  <br/> |
|Sheet4 の値 100 は、「Constant」として定義されています。  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<�ȗ�\>  <br/> |"Constant"  <br/> |
|Sheet4 の指定の数式には「SumTotal」という名前が付いています。  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<�ȗ�\>  <br/> |"SumTotal"  <br/> |
|アクティブなシートの非表示名「Counter」として 3 が定義されています。  <br/> |"3"  <br/> |\<省略\>  <br/> |2   <br/> |"Counter"  <br/> |
   
## <a name="see-also"></a>関連項目

- [xlfGetName](xlfgetname.md)
- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

