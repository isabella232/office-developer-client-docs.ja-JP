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
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798971"
---
# <a name="xlfgetname"></a>xlfGetName

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**[名前の管理]** ダイアログ ボックスの **[参照範囲]** 列に表示される名前の定義を返します。このダイアログ ボックスは、**[数式]** タブの **[定義された名前]** セクションで **[名前の管理]** をクリックすると表示されます。定義に参照が含まれている場合、参照は R1C1 形式の参照として示されます。 **xlfGetName** を使用して、名前で定義されている値を確認します。 定義に対応する名前を取得するには、[xlfGetDef](xlfgetdef.md) を使用します。
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>パラメーター

_pxNameText_ (**xltypeStr**)
  
シートで定義されている名前、アクティブなブックで定義されている名前への外部参照 (`"!Sales"` など)、または開いているブックで定義されている名前への外部参照 (`"[Book1]SHEET1!Sales"` など) にできます。  また _pxNameText_は非表示にできます。 
  
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

