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
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="ede2e-103">Outlook アイテムが変更されたが、(Outlook の補助参照) が保存されていないかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ede2e-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="ede2e-104">このトピックは、項目が変更されているし、保存されていないかどうかを確認するのには、Outlook アイテムに対応するプロパティを呼び出し、 **dispidFDirty**のディスパッチ ID を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ede2e-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="ede2e-105">アイテム オブジェクトを指定して、 [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx)メソッドを使用して、 [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx)インターフェイス ポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="ede2e-105">Given an item object, you can use the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) method to obtain an [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) interface pointer.</span></span> <span data-ttu-id="ede2e-106">トピックには、関数`FIsItemDirty` _pdisp_、入力パラメーターとして、 **IDispatch**ポインターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="ede2e-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="ede2e-107">`FIsItemDirty`では、項目が変更されたかどうかを確認するには、フラグ [](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx)の **wFlags**を _dispIdMember_のパラメーターの引数として `DISPATCH_METHOD | DISPATCH_PROPERTYGET`を指定する _:invoke_メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ede2e-107">`FIsItemDirty` calls the [IDispatch::Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="ede2e-108">`FIsItemDirty`ブール値を返します (**該当**項目に変更が保存されていないがそれ以外の場合、 **false を指定**)。</span><span class="sxs-lookup"><span data-stu-id="ede2e-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="ede2e-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="ede2e-109">See also</span></span>

- [<span data-ttu-id="ede2e-110">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="ede2e-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

