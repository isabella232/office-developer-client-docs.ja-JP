---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436630"
---
# <a name="xlfgetname"></a>xlfGetName

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references. Use **xlfGetName** to check the value defined by a name. To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>パラメーター

_pxNameText_ (**xltypeStr**)
  
Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.  _pxNameText_ can also be a hidden name. 
  
_pxInfoType_ (**xltypeBool**)
  
名前について返される情報の種類を指定します。**FALSE** または省略すると、定義が返されます。**TRUE** の場合、名前がシートに対してのみ定義されていると **TRUE** を返し、名前がブック全体に対して定義されていると **FALSE** を返します。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

_pxRes_ (**xltypeStr**、**xltypeBool**、または **xltypeErr**)
  
_pxInfoType_ に渡された値に応じて、指定した名前の定義 (**xltypeStr**)、あるいは **TRUE** または **FALSE** (**xltypeBool**) が返されます。
  
## <a name="remarks"></a>注釈

**[シートの保護]** ダイアログ ボックスで **[シートとロックされたセルの内容を保護する]** チェック ボックスを選択して対象の名前が含まれるブックを保護した場合、**xlfGetName** は `#N/A` エラー値を返します。**[シートの保護]** ダイアログ ボックスを表示するには、**[校閲]** タブの **[変更]** セクションにある **[シートの保護]** をクリックします。 
  
次の表に、特定の _pxNameText_ 引数を指定して.**xlfGetDef** を呼び出した場合に返される値の例を 3 つ示します。 
  
|**Excel における定義**|**_pxNameText_**|**戻り値**|
|:-----|:-----|:-----|
|シートで名前 [Sales] が数値 523 として定義されています。  <br/> |"Sales"  <br/> |"=523"  <br/> |
|アクティブなシートで名前 [Profit] が、数式 =Sales-Costs として定義されています。  <br/> |"!Profit"  <br/> |"=Sales-Costs"  <br/> |
|アクティブ シートで名前 [Database] が、範囲 A1:F500 として定義されています。  <br/> |"!Database"  <br/> |"=R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>関連項目

- [xlfGetDef](xlfgetdef.md)
- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

