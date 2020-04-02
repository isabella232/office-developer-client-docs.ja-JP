---
title: Outlook アイテムが変更されたが、保存されていないかどうかを判断する (Outlook 補助リファレンス)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 dispidFDirtyのディスパッチ ID を使用する方法を示します。
ms.openlocfilehash: 5dc20a45342e0434ab19d7c2347e98dec27b61b8
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102948"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Outlook アイテムが変更されたが、保存されていないかどうかを判断する (Outlook 補助リファレンス)

このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 **dispidFDirty**のディスパッチ ID を使用する方法を示します。 
  
アイテム オブジェクトを指定して、 [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))メソッドを使用して、 [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)インターフェイス ポインターを取得できます。 トピック`FIsItemDirty`内の関数は、入力パラメーターとして**IDispatch**ポインター _pdisp_を受け入れます。  `FIsItemDirty`では、項目が変更されたかどうかを確認するには、フラグ [](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)の **wFlags**を _dispIdMember_のパラメーターの引数として `DISPATCH_METHOD | DISPATCH_PROPERTYGET`を指定する _:invoke_メソッドを呼び出します。  `FIsItemDirty`ブール値を返します (**True**を指定すると、アイテムの変更が保存されていないことを示します。それ以外の場合は**False**)。
  
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

