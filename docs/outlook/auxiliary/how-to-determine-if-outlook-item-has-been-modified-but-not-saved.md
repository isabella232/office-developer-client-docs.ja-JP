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
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="2c372-103">Outlook アイテムが変更されたが、保存されていないかどうかを判断する (Outlook 補助リファレンス)</span><span class="sxs-lookup"><span data-stu-id="2c372-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="2c372-104">このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 **dispidFDirty**のディスパッチ ID を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2c372-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="2c372-105">アイテム オブジェクトを指定して、 [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))メソッドを使用して、 [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)インターフェイス ポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="2c372-105">Given an item object, you can use the [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface pointer.</span></span> <span data-ttu-id="2c372-106">トピック`FIsItemDirty`内の関数は、入力パラメーターとして**IDispatch**ポインター _pdisp_を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="2c372-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="2c372-107">`FIsItemDirty`では、項目が変更されたかどうかを確認するには、フラグ [](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)の **wFlags**を _dispIdMember_のパラメーターの引数として `DISPATCH_METHOD | DISPATCH_PROPERTYGET`を指定する _:invoke_メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2c372-107">`FIsItemDirty` calls the [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="2c372-108">`FIsItemDirty`ブール値を返します (**True**を指定すると、アイテムの変更が保存されていないことを示します。それ以外の場合は**False**)。</span><span class="sxs-lookup"><span data-stu-id="2c372-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="2c372-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c372-109">See also</span></span>

- [<span data-ttu-id="2c372-110">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="2c372-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

