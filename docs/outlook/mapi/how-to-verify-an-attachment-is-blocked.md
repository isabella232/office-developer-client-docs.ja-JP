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
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="8e3a4-103">添付ファイルがブロックされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e3a4-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="8e3a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e3a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e3a4-105">C++ では、このコード サンプルを使用する方法を示しています、 [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md)インターフェイスを表示して、インデックス作成の Microsoft Outlook 2010 または Microsoft Outlook 2013 で添付ファイルがブロックされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e3a4-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="8e3a4-106">[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md)は、 [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスから派生します。</span><span class="sxs-lookup"><span data-stu-id="8e3a4-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="8e3a4-107">取得することができます、 [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) 、MAPI セッションを要求しているオブジェクト**IID_IAttachmentSecurity**の[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出して、インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="8e3a4-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="8e3a4-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)場合**true**を返します_pfBlocked_の添付ファイルが Outlook 2010 または Outlook 2013 で安全でないと見なされ、表示して、Outlook 2010 または Outlook 2013 でのインデックス作成用にブロックされています。</span><span class="sxs-lookup"><span data-stu-id="8e3a4-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
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


