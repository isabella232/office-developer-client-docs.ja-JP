---
title: Outlook アイテムが変更されたが、(Outlook の補助参照) が保存されていないかどうかを決定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 dispidFDirtyのディスパッチ ID を使用する方法を示します。
ms.openlocfilehash: ece6ede368cf2ffb3b18575161fef4b3f132fdf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799315"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Outlook アイテムが変更されたが、(Outlook の補助参照) が保存されていないかどうかを決定します。

このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 **dispidFDirty**のディスパッチ ID を使用する方法を示します。 
  
アイテム オブジェクトを指定して、 [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx)メソッドを使用して、 [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx)インターフェイス ポインターを取得できます。 トピックには、関数`FIsItemDirty` _pdisp_、入力パラメーターとして、 **IDispatch**ポインターを受け取ります。  `FIsItemDirty`では、項目が変更されたかどうかを確認するには、フラグ [](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx)の **wFlags**を _dispIdMember_のパラメーターの引数として `DISPATCH_METHOD | DISPATCH_PROPERTYGET`を指定する _:invoke_メソッドを呼び出します。  `FIsItemDirty`ブール値を返します (**該当**項目に変更が保存されていないがそれ以外の場合、 **false を指定**)。
  
```cpp
bool FIsItemDirty(IDispatch *pdisp)
{
    DISPPARAMS dispparams;
    UINT uArgErr;
    HRESULT hr = S_OK;
    CComVariant varDirty;
    dispparams.rgvarg = 0;
    dispparams.cArgs = 0;
    dispparams.cNamedArgs = 0;
    dispparams.rgdispidNamedArgs = NULL;
    hr = pdisp->Invoke(dispidFDirty,
        IID_NULL,
        LOCALE_SYSTEM_DEFAULT,
        DISPATCH_METHOD | DISPATCH_PROPERTYGET,
        &amp;dispparams,
        &amp;varDirty,
        NULL,
        &amp;uArgErr);
    return SUCCEEDED(hr) &amp;&amp; varDirty.bVal;
}

```

## <a name="see-also"></a>関連項目

- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)

