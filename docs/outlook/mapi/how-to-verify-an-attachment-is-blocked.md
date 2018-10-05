---
title: 添付ファイルがブロックされていることを確認します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393839"
---
# <a name="verify-an-attachment-is-blocked"></a>添付ファイルがブロックされていることを確認します。

**適用対象**: Outlook 2013 | Outlook 2016 
  
C++ では、このコード サンプルを使用する方法を示しています、 [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md)インターフェイスを表示して、インデックス作成の Microsoft Outlook 2010 または Microsoft Outlook 2013 で添付ファイルがブロックされているかどうかを確認します。 
  
[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md)は、 [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスから派生します。 取得することができます、 [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) 、MAPI セッションを要求しているオブジェクト**IID_IAttachmentSecurity**の[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出して、インターフェイスです。 [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)場合**true**を返します_pfBlocked_の添付ファイルが Outlook 2010 または Outlook 2013 で安全でないと見なされ、表示して、Outlook 2010 または Outlook 2013 でのインデックス作成用にブロックされています。 
  
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


