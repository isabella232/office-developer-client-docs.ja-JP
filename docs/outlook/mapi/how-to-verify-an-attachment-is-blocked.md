---
title: 添付ファイルがブロックされていることを確認します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: a21383e0ea6920075a57d872e82851462bf0e8d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800260"
---
# <a name="verify-an-attachment-is-blocked"></a>添付ファイルがブロックされていることを確認します。

**適用されます**: Outlook 
  
C++ では、このコード サンプルを使用する方法を示しています、 [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md)インターフェイスを表示して、インデックス作成の Microsoft Outlook 2010 または Microsoft Outlook 2013 で添付ファイルがブロックされているかどうかを確認します。 
  
[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md)は、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx)インターフェイスから派生します。 取得することができます、 [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) 、MAPI セッションを要求しているオブジェクト**IID_IAttachmentSecurity**の[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)を呼び出して、インターフェイスです。 [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)場合**true**を返します_pfBlocked_の添付ファイルが Outlook 2010 または Outlook 2013 で安全でないと見なされ、表示して、Outlook 2010 または Outlook 2013 でのインデックス作成用にブロックされています。 
  
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


