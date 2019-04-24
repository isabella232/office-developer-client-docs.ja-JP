---
title: outlook アイテムが変更されたが、保存されていないかどうかを判断する (outlook 補助リファレンス)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 dispidFDirtyのディスパッチ ID を使用する方法を示します。
ms.openlocfilehash: e66a23983a3cc19a7cb51d4b4c3b2c1cee58a793
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317641"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>outlook アイテムが変更されたが、保存されていないかどうかを判断する (outlook 補助リファレンス)

このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 **dispidFDirty**のディスパッチ ID を使用する方法を示します。 
  
アイテム オブジェクトを指定して、 [IUnknown::QueryInterface](https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_))メソッドを使用して、 [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)インターフェイス ポインターを取得できます。 トピック`FIsItemDirty`内の関数は、入力パラメーターとして**IDispatch**ポインター _pdisp_を受け入れます。  `FIsItemDirty`では、項目が変更されたかどうかを確認するには、フラグ [](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)の **wFlags**を _dispIdMember_のパラメーターの引数として `DISPATCH_METHOD | DISPATCH_PROPERTYGET`を指定する _:invoke_メソッドを呼び出します。  `FIsItemDirty`ブール値を返します (**True**を指定すると、アイテムの変更が保存されていないことを示します。それ以外の場合は**False**)。
  
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

