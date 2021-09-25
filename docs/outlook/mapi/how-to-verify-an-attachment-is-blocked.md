---
title: 添付がブロックされていることを確認する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 57c7c3861073910a1f5331c71e9e5ecc1c0c83a0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576199"
---
# <a name="verify-an-attachment-is-blocked"></a>添付がブロックされていることを確認する

**適用対象**: Outlook 2013 | Outlook 2016 
  
C++ のこのコード サンプルは[、IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md)インターフェイスを使用して、Microsoft Outlook 2010 または Microsoft Outlook 2013 が表示およびインデックス作成のために添付ファイルをブロックするかどうかを確認する方法を示しています。 
  
[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) は [IUnknown インターフェイスから派生](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) します。 [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md)インターフェイスを取得するには、MAPI セッション オブジェクトで [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出し、そのインターフェイスを要求 **IID_IAttachmentSecurity。** [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)は、添付ファイルが Outlook 2010 または Outlook 2013 によって安全でないと見なされ、Outlook 2010 または Outlook 2013 で表示およびインデックス作成がブロックされている場合 _、pfBlocked_ で true を返します。 
  
```cpp
HRESULT IsAttachmentBlocked(LPMAPISESSION lpMAPISession, LPCWSTR pwszFileName, BOOL* pfBlocked) 
{ 
    if (!lpMAPISession || !pwszFileName || !pfBlocked) return MAPI_E_INVALID_PARAMETER; 
 
    HRESULT hRes = S_OK; 
    IAttachmentSecurity* lpAttachSec = NULL; 
    BOOL bBlocked = false; 
 
    hRes = lpMAPISession-&gt;QueryInterface(IID_IAttachmentSecurity,(void**)&amp;lpAttachSec); 
    if (SUCCEEDED(hRes) &amp;&amp; lpAttachSec) 
    { 
        hRes = lpAttachSec-&gt;IsAttachmentBlocked(pwszFileName,&amp;bBlocked); 
    } 
    if (lpAttachSec) lpAttachSec-&gt;Release(); 
 
    *pfBlocked = bBlocked; 
    return hRes; 
}

```


